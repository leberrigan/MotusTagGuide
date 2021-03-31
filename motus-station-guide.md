[<u>Tag basics</u>](#tag-basics)

> [<u>What are radio tags?</u>](#what-are-radio-tags)
>
> [<u>How do radio tags compare to other tracking
> technologies?</u>](#how-do-radio-tags-compare-to-other-tracking-technologies)

[<u>Tag Selection</u>](#tag-selection)

> [<u>Detecting Movement</u>](#detecting-movement)
>
> [<u>Deploying Tags in the Motus
> Network</u>](#deploying-tags-in-the-motus-network)
>
> [<u>Tag Types</u>](#tag-types)

[<u>How Tags Work</u>](#how-tags-work)

> [<u>What is a tag or radio
> transmitter?</u>](#what-is-a-tag-or-radio-transmitter)
>
> [<u>What types of tags are there?</u>](#what-types-of-tags-are-there)
>
> [<u>Lotek Radio Tags</u>](#lotek-radio-tags)
>
> [<u>Tag Pulses</u>](#tag-pulses)
>
> [<u>Pulse Intervals and Bursts</u>](#pulse-intervals-and-bursts)
>
> [<u>Burst Intervals</u>](#burst-intervals)

[<u>How to Locate Tags with Manual
Tracking</u>](#how-to-locate-tags-with-manual-tracking)

> [<u>Manual tracking basics</u>](#manual-tracking-basics)
>
> [<u>Retrieving lost tags</u>](#retrieving-lost-tags)

[<u>Aliasing</u>](#aliasing)

> [<u>Type 1: False burst interval</u>](#type-1-false-burst-interval)
>
> [<u>Conditions</u>](#conditions)
>
> [<u>Type 2: False Lotek Tag ID</u>](#type-2-false-lotek-tag-id)
>
> [<u>Conditions</u>](#conditions-1)
>
> [<u>Type 3: False Burst Interval and Lotek Tag
> ID</u>](#type-3-false-burst-interval-and-lotek-tag-id)
>
> [<u>Conditions</u>](#conditions-2)
>
> [<u>How can we eliminate aliasing? \[STILL NEEDS
> WORK!\]</u>](#how-can-we-eliminate-aliasing-still-needs-work)
>
> [<u>Context</u>](#context)
>
> [<u>Location</u>](#location)
>
> [<u>Timing</u>](#timing)
>
> [<u>Other detections</u>](#other-detections)
>
> [<u>Tag Parameters</u>](#tag-parameters)
>
> [<u>Signal strength</u>](#signal-strength)
>
> [<u>Frequency offset</u>](#frequency-offset)
>
> [<u>Number of skipped bursts</u>](#number-of-skipped-bursts)
>
> [<u>Burst interval slop</u>](#burst-interval-slop)
>
> [<u>Run length</u>](#run-length)

# Tag basics

This section deserves its own guide - we’re working on it. For now it
lives here.

## What are radio tags?

While tags can refer to many different things, in this document we are
talking about miniaturized radio transmitters that weigh as little as
0.15 g so they can be affixed to birds, bats, and even insects. Tags are
made such that they each emit a slightly different radio signal allowing
animals to be tracked individually by using a receiver.

## How do radio tags compare to other tracking technologies?

There are several other ways animals can be tracked, each of which have
their advantages and disadvantages. For a detailed summary of tracking
technologies see - (insert references., eg. Bridge et al.,)The first
method of tracking was through banding/ringing which is still done to
this day, but it is unreliable with a very low recapture rate. Colour
banding can be very effective for tracking certain species where the
search area is relatively small (e.g.: breeding passerines in a plot or
migratory shorebirds confined to specific beaches).

For electronic tracking techniques, radar can be used to detect large
movements of many birds at once without the need to directly affect
anything, but individuals and species cannot be distinguished.

Passive integrated transponders (i.e.; PIT tags or Passive RFID) are a
type of transmitter that does not require a battery and are instead
powered by the presence of a strong magnetic field, similar to security
devices found in items at retail stores. Due to the requirement of a
strong magnetic field, these devices only operate in close proximity to
a receiver which is useful for detecting movement within a narrow
passage (i.e.; a burrow or river), but impractical for detecting aerial
movements. Active RFID tags use a battery for the same effect and have a
greater range, but typically only in the 10’s to 100’s of meters.

Light-level Geolocators (GLS tags) are a popular choice , first used by
Dr. Bridget Stutchbury in Ovenbirds, they offer a method for
geopositioning small migratory wildlife without the need of any
receivers, instead data is logged on a small memory chip which must be
retrieved from the animal. This means GLS tags are only practical when
the target individuals can reliably be re-trapped some time after they
have been deployed. In addition, GLS tags use a combination of daylength
and relative timing of sunrise and sunset to determine their geographic
position which can have widely variable levels of precision making them
most useful for detecting broad scale movements.

GPS and satellite tags both use GPS to record locations, but there are
several different methods for data to be retrieved once it has been
recorded. Certain GPS tags, like the PinPoint, function similarly to GLS
tags, requiring physical retrieval of the tag to download data, but use
more reliable satellite triangulation to gain position information.

The more advanced satellite tags will transmit data directly to a
satellite which is then transmitted back to a base station on land, like
Icarus tags. Although these tags can provide the high precision tracking
data from anywhere on the globe without the need of re-trapping, it
comes at the price of increased weight and cost making them unviable for
small passerines, most bats, and insects.

Cellular Tracking Technologies has gone a step in between and uses a
Cellular (Global System for Mobile Communication - GSM) tags transmite
GSM to communicate GPS and other data to nearby cellular towers,
offering lower cost data acquisition, but weight can is still an issue,
making this technology not suitable for most passerines, bats, and
insects.

The niche for radio transmitters like the ones we use in Motus fits
where there are limits in the size or cost of tags. Their main
restriction is that they can only be tracked where receivers exist and
installing stations can be expensive. That’s why it’s so important to
have a collaborative network of receivers for this type of technology.

| **Tracker type**                        | **Track individuals** | **Minimum weight** | **Cost**                | **Data acquired by** | **Power source**      |
|-----------------------------------------|-----------------------|--------------------|-------------------------|----------------------|-----------------------|
| **Bands**                               | Yes                   | \~0 g              | \~$0                    | Bander               | N/A                   |
| **Radar**                               | No                    | N/A                | \~$20k-$40k<sup>1</sup> | Radar station        | N/A                   |
| **PIT tags**                            | Yes                   |                    |                         | Receiver             | Strong magnetic field |
| **Active RFID**                         | Yes                   |                    |                         | Receiver             | Battery               |
| **GLS**                                 | Yes                   |                    | \~$200                  | Tag                  | Battery               |
| **GPS Pinpoint**                        | Yes                   |                    |                         | Tag                  | Battery               |
| **GPS Satellite**                       | Yes                   |                    |                         | Satellite            | Battery               |
| **GPS Cellular**                        | Yes                   |                    |                         | Cell Station         | Battery               |
| **Beeper tags**                         | Yes                   |                    | \~$200<sup>2</sup>      | Receiver             | Battery               |
| **Digitally encoded radio transmitter** | Yes                   | 0.15 g             | \~$200<sup>2</sup>      | Receiver             | Battery and/or solar  |

#  

# Tag Selection

## Detecting Movement

As students of migration ecology, we ultimately seek the ability to know
everything about all individuals at all times. Unfortunately, the
technology required to do this for most flying migratory animals,
particularly the smallest bodied ones, does not exist. Therefore,
biologists have to use a combination of *complementary* tools such as
tracking-based geolocators, GPS and GSM, GPS and Geolocation data
loggers, as well as isoptopic, genetic, and good old bird
banding/ringing to discover the complete life histories of migratory
animals. While often viewed as having competing value, these tools are
undeniably complementary, and researchers need to employ the best tool
for the job given the specific questions and study system in mind.

What is most unique about Motus is that it provides an opportunity to
track the widest variety of the smallest animals possible, *today*, at
local, regional, or hemispheric scales depending on the location and
species in question. And best of all, almost anyone can get involved in
one way or another – Motus is the ultimate hands-on community science
project.

Another important differentiation between automated radio telemetry and
other technologies available is that the temporal precision of the data
can be much greater with radio telemetry as tags can repeat their
signals as quickly as every 2 seconds. This extremely high temporal
precision can allow for exceptionally detailed examinations of an
animals behavior, movement patterns, direction and speed of flight.

The selection of specific tag type will largely depend on the spatial
temporal scale of your study as well as your study species and
geography.

## Deploying Tags in the Motus Network

The study location may largely determine what type of data you can
expect, and which tags to use. When setting up your study, it’s
important to consider how your tags may be detected by receivers in your
area of interest. One tactic employed by the [<u>Northeast Motus
Collaboration</u>](https://www.northeastmotus.com/) is to build a
receiver ‘fence’ over a geographic area such that any tagged animal
passing through it will get detected. In Ontario, where many more
stations are available, there is a grid of stations (or series of
fences) to allow for better spatial resolution of movements. In the end,
you will need to decide what works best for your region based on
migratory flyways, foraging locations, your goals, funding, and the
location of nearby receivers.

Go to the [<u>receivers map</u>](https://motus.org/data/receiversMap) to
see all currently active receivers, what frequency they operate on and
which type of tags they can detect. Keep in mind that these receivers
have been deployed by various researchers who check their stations at
different times. It’s helpful to check the ‘last data processed’ to get
an idea of how often these stations get checked – you don’t want to be
stuck waiting for a station you don’t own to get checked! In addition,
stations that haven’t been checked in a long time (6 months to a year)
may be in various states of disrepair so it’s also best not to rely on
these stations before contacting the project manager.

## 

## Tag Types

Motus supports two types of uniquely coded radio transmitters: NanoTags™
manufactured by [<u>Lotek Wireless Inc</u>](http://lotek.com/),
operating on frequencies 166.380 MHz (Western Hemisphere), 150.100 MHz
(Europe), and 151.500 MHz (Australia), and LifeTag™ and PowerTags™
manufactured by [<u>Cellular Tracking
Technologies</u>](http://www.celltracktech.com/) (CTT) operating on 434
MHz globally. The two tags use fundamentally different transmission and
coding systems. Nanotags tags use amplitude modulation, or AM, whereas
CTT tags us frequency modulation, or FM. Nanotags emit 4-bit pules that
encode a unique ID in the time difference between these pulses, called
Pulse-position Modulation (PPM). CTT use frequency-shift keying (FSK)
which flips between two similar frequencies to encode a binary “1” or
“0”, with a total of 64 of these bits per transmission.

The distribution of stations listening for either tag is not uniform, so
collaborators should consult the [<u>Motus Receiver
Map</u>](https://motus.org/data/receiversMap/) to confirm which
frequency stations are operating on throughout the network. When
communicating with Lotek or CTT, be sure to explicitly state that you
want your tags/system to be compatible with Motus.

It is simple to outfit some Motus receivers to be dual-mode in order to
“listen” for both of these tag types. We recommend that stations be
configured this way whenever possible in order to support the greatest
number of researchers.

There is a lot of detail about these two tags that can’t all be explored
here, but the table below summarizes the major differences. [<u>Contact
Motus</u>](https://motus.org/selection-guide/contact), or the tag
providers above for more information.

<table>
<thead>
<tr class="header">
<th></th>
<th><p><a href="https://www.lotek.com/products/nanotags/"><strong><u>Lotek Nanotag</u></strong></a></p>
<p><img src="media\image4.jpg" style="width:1.14063in;height:1.14063in" alt="Lotek Nanotag" /></p></th>
<th><p><strong><u>Lotek Nanotag Solar</u></strong></p>
<p><img src="media\image3.jpg" style="width:1.07813in;height:1.07813in" alt="Lotek Nanotag Solar" /></p></th>
<th><p><strong><u>CTT LifeTags</u></strong></p>
<p><img src="media\image9.png" style="width:1.05729in;height:1.05729in" alt="CTT LifeTags" /></p></th>
<th><p><strong><u>CTT PowerTags</u></strong></p>
<p><img src="media\image10.png" style="width:1.14063in;height:1.14063in" alt="CTT PowerTags" /></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Manufacturer</strong></td>
<td><strong>Lotek</strong></td>
<td><strong>Lotek</strong></td>
<td><strong>CTT</strong></td>
<td><strong>CTT</strong></td>
</tr>
<tr class="even">
<td>Frequency</td>
<td>150.1, 151.5, or 166.380 MHz</td>
<td>150.1, 151.5, or 166.38 MHz</td>
<td>434 MHz</td>
<td>434 MHz</td>
</tr>
<tr class="odd">
<td>Lifespan</td>
<td>Long (20 – 2000 d)</td>
<td>Unlimited</td>
<td>Unlimited</td>
<td>Long (180 d to yrs)</td>
</tr>
<tr class="even">
<td>Daily active period</td>
<td>24/7 or alternate 12-hour on/off</td>
<td>24/7 (battery and solar powered)</td>
<td>Only in direct sunlight (solar powered)</td>
<td>24/7</td>
</tr>
<tr class="odd">
<td>Weight</td>
<td>0.15 g – 3.00 g</td>
<td>1.4 g and up</td>
<td>0.44 g and up</td>
<td>0.33 g and up</td>
</tr>
<tr class="even">
<td>Smallest bird (%3 body weight)</td>
<td>5.0 g</td>
<td>46.7 g</td>
<td>14.7 g</td>
<td>11.0 g</td>
</tr>
<tr class="odd">
<td>Possible number of unique tags</td>
<td>&gt;36,000*</td>
<td>&gt;36,000*</td>
<td>~4 billion</td>
<td>~ 4 billion</td>
</tr>
<tr class="even">
<td>Burst intervals</td>
<td>~2-40 seconds</td>
<td>Similar to CTT (may diminish with power loss) [needs more information]</td>
<td>2 seconds (configurable)</td>
<td>Programmable: from 1 sec up</td>
</tr>
<tr class="odd">
<td>Current number of compatible Motus Stations</td>
<td><p>900+</p>
<p><a href="https://motus.org/data/receiversMap/"><u>See receiver map for distribution</u></a></p></td>
<td><p>90+</p>
<p><a href="https://motus.org/data/receiversMap/"><u>See receiver map for distribution</u></a></p></td>
<td><p>79+</p>
<p><a href="https://motus.org/data/receiversMap/"><u>See receiver map for distribution</u></a></p></td>
<td><p>79+</p>
<p><a href="https://motus.org/data/receiversMap/"><u>See receiver map for distribution</u></a></p></td>
</tr>
<tr class="even">
<td>Compatible with CTT Receivers</td>
<td>SensorStation with FUNcube Dongle only</td>
<td>SensorStation with FUNcube Dongle only</td>
<td>Yes</td>
<td>Yes</td>
</tr>
<tr class="odd">
<td>Compatible with Lotek Receivers</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
<td>No</td>
</tr>
<tr class="even">
<td>Compatible with SensorGnome Receivers</td>
<td>With FUNcube dongle only</td>
<td>With FUNcube dongle only</td>
<td>With CTT Motus Adapter only</td>
<td>With CTT Motus Adapter only</td>
</tr>
<tr class="odd">
<td>Price</td>
<td>~$200 USD</td>
<td>~$200 USD</td>
<td>~$200 USD</td>
<td>~$200 USD</td>
</tr>
<tr class="even">
<td>Discount</td>
<td>Contact Lotek</td>
<td>Contact Lotek</td>
<td><p>5% for 20+</p>
<p>10% for 30+</p></td>
<td><p>5% for 20+</p>
<p>10% for 30+</p></td>
</tr>
<tr class="odd">
<td><strong>* This number is calculated by multiplying the number of unique ID’s emitted by Lotek tags (517) with the number of unique burst intervals available (70). These burst intervals range from 2.3 to 39.7 seconds, which corresponds to the number of primes between 23 and 397 such that no two burst intervals overlap with one another.</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

#  

# How Tags Work

## What is a tag or radio transmitter?

When most people use the word “tag” usually they’re talking about a
clothing label or a sticker on a banana, but more generally it’s a type
of marker which identifies the item in some way. This is no different
from the way we use the word except in this instance we are using a
radio transmitter as a marker. A **radio transmitter** is an electronic
device which sends information through radio waves, similar to radio
stations used to broadcast music to your car. The radio transmitters
used in the Motus Wildlife Tracking Network are specially designed to be
as small and lightweight as possible, allowing scientists to attach them
to small animals without harming them. The signal transmitted by these
transmitters, or “tags”, contains a special code which uniquely
identifies the device. This signal is picked up by radio receiver
stations which are placed in strategic locations across the globe. To
Learn more about these receiver stations, **click here**.

## What types of tags are there?

There are two main types of signals transmitted by radio tags used in
the Motus Wildlife Tracking Network. Tags produced by Lotek transmit a
pulse-position modulated (PPM) signal with 4 pulses at 166.380 MHz; tags
produced by CTT transmit a 64-bit Frequency shift keying signal at 434
MHz. See the sections below for more information on each tag make.

## Lotek Radio Tags

To encode a unique ID, Lotek radio tags transmit a series of pulses at
166.380 MHz (in the Americas; other regions differ).

### Tag Pulses

A tag pulse consists of a single, 20 millisecond (ms) long radio
transmission sent by the tag. Individual pulses are the raw data that
SensorGnome receivers record.

<img src="media\image1.png" style="width:6.3in;height:1.67495in" />

### Pulse Intervals and Bursts

A pulse interval is the time between two successive pulses. It is
measured in milliseconds (ms). Tags emit four pulses at a time, together
making a **burst**. The pulse interval is what we use to encode the
**Lotek Tag ID**. This is measured to a high level of precision,
allowing for just 1.5 ms of variation summed across all pulse intervals
in a burst.

<img src="media\image5.png" style="width:4.5in;height:1.72711in" />

*Note: these pulse intervals do not reflect properties of real tags are
intended for demonstration purposes only.*

### Burst Intervals

A burst interval is the timing between successive bursts. It is measured
in seconds.

The burst interval and **Lotek Tag ID** combined are used to encode the
**Motus Tag ID**. To avoid ambiguous detections, burst intervals cannot
be integer multiples of one another. Therefore, all burst intervals must
be *prime factors.* Keep in mind there must be two successive bursts to
measure the burst interval and associate a **Motus Tag ID**, but
[<u>some bursts can be
skipped.</u>](https://docs.google.com/document/d/1IIXoSF32fBOuva3-WZXm1bRuG_08kAFV/edit#heading=h.3znysh7)
Bursts are measured to a high level of precision, allowing for [<u>just
4 ms of
‘slop’.</u>](https://docs.google.com/document/d/1IIXoSF32fBOuva3-WZXm1bRuG_08kAFV/edit#heading=h.2et92p0)

<img src="media\image8.png" style="width:4.55in;height:1.50271in" />

#  

# How to Locate Tags with Manual Tracking

## Manual tracking basics

\[placeholder\]

## Retrieving lost tags

Lotek NanoTags can be retrieved by manually tracking the tag with a
Lotek handheld receiver. Since these receivers have a long range at full
gain, it can take a long time to locate a tag that has been lost, but
manual tracking is still routine for researchers . When touching the
ground, the tag signal is modulated enough that a trained ear can
actually identify the tag as being detached just by the quality of the
audio signal the receiver emits.

Without a Lotek receiver you can use the open-source SensorGnome
receivers instead, but they are much more difficult to use in this way
since there is a longer time delay between when a detection occurs and
when it shows up on the receiver’s display. Further, SensorGnome
receivers do not offer a real-time gain adjustment, whereas Lotek
receivers do.  
  
\[Insert information on CTT Tags\]  
  
\[Insert methods for retrieving tags\]

## 

#  

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
