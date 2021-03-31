
# Aliasing

Tag aliasing is a method by which false detections of a tag can occur
because of overlapping signals being received from multiple real tags.
To understand tag aliasing, it is important to understand how tags
encode their unique ID and how we interpret the signals they produce.
This document only refers to Lotek NanoTags as we have not had reports
of aliasing with CTT tags. Before reading this section, make sure you
have a solid understanding of [<u>How tags work</u>](#_gaa1klaz85r).

Tag aliasing can occur when multiple real tags are transmitting tag
pulses at the same Motus station and over the same period of time. An
aliased tag results in an erroneous **Motus Tag ID** being allocated to
a set of **tag pulses**.

The **Motus Tag ID** relies on two identifiers to create a unique ID:
the **Lotek Tag ID**, which consists of multiple pulse intervals within
a single burst; and the **burst interval**.

Aliasing occurs when an erroneous **Lotek Tag ID** and/or an erroneous
**burst interval** is associated with a set of **tag pulses**. There are
three known types of tag aliasing listed below.

## Type 1: False burst interval

This type of aliasing should be rare but can occur if two tags with the
same Lotek ID are deployed at the same time. Type 1 aliasing can also
occur—although much rarer—when tagged animals move to a new location
where another tag with the same Lotek ID happens to be.

### Conditions

-   Multiple real tags with the **same Lotek Tag ID** are detected.

-   Aliased tags also have the **same Lotek Tag ID**, but a **different
    > burst interval**.

<img src="media\image7.png" style="width:6.30208in;height:1.19792in" />
<img src="media\image7.png" style="width:6.30208in;height:1.41667in" />
<img src="media\image7.png" style="width:6.30208in;height:2.13542in" />

*Note: colours are intended as an visual aid and are not some type of
identifier transmitted in the signal.*

## Type 2: False Lotek Tag ID

This is the most common type of type of aliasing. Typically occurs when
banding many individuals at once where those individuals stay near one
another after release, such as in a colony or with shorebirds. Tags are
never activated at the exact same time so we should expect a slight
offset in the timing of bursts. For this reason, a smaller number of
tags will also have a smaller chance of overlapping bursts. Similarly,
longer burst intervals also reduce the probability of bursts
overlapping.

### Conditions

-   Multiple real tags with the **same burst interval** are detected.

-   Aliased tags also have the **same burst interval**, but a different
    > **Lotek Tag ID**.

<img src="media\image6.png" style="width:6.30208in;height:1.13661in" />

<img src="media\image6.png" style="width:6.30208in;height:1.17708in" />

<img src="media\image6.png" style="width:6.30208in;height:1.16667in" />

<img src="media\image6.png" style="width:6.30208in;height:1.14583in" />

*Note: colours are intended as an visual aid and are not some type of
identifier transmitted in the signal.*

## Type 3: False Burst Interval and Lotek Tag ID

This can occur under similar conditions as type 2 aliasing but is much
rarer since it relies on multiple tag bursts to overlap much more
precisely. The aliased tag burst interval will be equal to some multiple
of a real tag burst interval, plus or minus a small fraction of a
second. In this type of aliasing, one burst will consist of pulses from
just *one tag* and another burst will made up of pulses from *multiple
tags*. The Lotek ID will be the same as the tag with which it shares all
pulses in a burst.

### Conditions

-   Multiple real tags with the **same burst interval** are detected.

-   Aliased tags have a **different burst interval** but will likely
    > have the **same Lotek Tag ID of one tag**.

<img src="media\image2.png" style="width:6.30208in;height:5.5in" />

*Note: colours are intended as an visual aid and are not some type of
identifier transmitted in the signal.*

## How can we eliminate aliasing? \[STILL NEEDS WORK!\]

At first it may seem like aliasing is an intrinsic and unavoidable
aspect of this technology, but there exist several methods to overcome
it.

### Context

When aliased tag detections are recorded at a receiver, its often easy
to immediately determine they are false based on:

#### Location

> Is this somewhere we would expect the animal at this time of year?

#### Timing

> What is the average flight speed between receivers?

#### Other detections

-   Are there multiple other tags detected at this station at the same
    > time with the same ID **OR** burst interval?

-   Are many tags *briefly* detected at a similar time?

### Tag Parameters

Some properties of tags can be used to further distinguish them from one
another. Tags are built to a certain level of precision some of which
are measured during tag registration. These measurements reveal slight
differences between the characteristics of the signals emitted by each
tag which can aid in identification. One of the best methods to
eliminate false detections is to compare known real detections on the
same antenna with suspicious detections using these properties.

#### Signal strength

The signal strength of a burst is the averaged signal strength of each
of the four pulses which make up a burst. The standard deviation of a
burst indicates the variation in pulses.

-   Type 1 aliased detections should be made up of alternating bursts
    > between two different tags. In this way, we should expect the
    > overall signal strength of these tags to also alternate.

-   Type 2 aliased tag bursts are made up of a combination of pulses
    > from multiple tags so those should all have a high signal strength
    > standard deviation.

-   Type 3 aliased tag bursts alternate between a burst from a single
    > tag and a burst made up of a combination of tags. These detections
    > should alternate between low and high signal strength standard
    > deviation.

Keep in mind that if these tags are near one another (i.e., in a flock)
you should expect a smaller difference in signal strength between tag.

#### Frequency offset

> The difference between the nominal frequency (e.g.: 166.380 MHz) and
> the actual measured frequency of the tag pulses. This is measured in
> kHz with an associated standard deviation.
>
> We should expect similar results to signal strength measurements as
> above, however proximity to other tagged individuals should not make a
> difference.

#### Number of skipped bursts

In noisy environments or with weak signal, some tag bursts may not be
received entirely. We allow for a maximum of 60 bursts to be missed to
avoid losing too many detections. For instance, if a 4.7 s tag has two
bursts detected with three bursts missed in between them, we would
expect there to be 4.7 \* (1 + 3) = 18.8 s gap between the two bursts.

#### Burst interval slop

The maximum allowed variation in a burst interval. We filter out all
data with a slop greater than 4 ms.

#### Run length

A ‘run’ consists of a collection of bursts. The length of the run
(*runLen*) is a count of these bursts, not the length of time. A run may
include gaps where bursts were skipped and it will terminate once more
than 60 bursts have been skipped. False detections as a result of radio
noise usually have very short run lengths; however, aliased tags are
more likely to have long run lengths, so this is not always the most
useful parameter to look at, but they should still be noticeably shorter
than true detections. Since runs can include skipped bursts, it can be
helpful to calculate the longest group of consecutive bursts within each
run (*longRun*)and compare it to the maximum number of bursts that could
have been detected during the run’s time interval (*maxRun*). You should
expect to see the ratio of *longRun* to *runLen* and the ratio of
*maxRun* to *runLen* to be much smaller for aliased tags than real tags.
