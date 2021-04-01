# Tag Selection

## Detecting Movement

As students of migration ecology, we ultimately seek the ability to know everything about all individuals at all times. Unfortunately, the technology required to do this for most flying migratory animals, particularly the smallest bodied ones, does not exist. Therefore, biologists have to use a combination of _complementary_ tools such as tracking-based geolocators, GPS and GSM, GPS and Geolocation data loggers, as well as isoptopic, genetic, and good old bird banding/ringing to discover the complete life histories of migratory animals. While often viewed as having competing value, these tools are undeniably complementary, and researchers need to employ the best tool for the job given the specific questions and study system in mind.

What is most unique about Motus is that it provides an opportunity to track the widest variety of the smallest animals possible, _today_, at local, regional, or hemispheric scales depending on the location and species in question. And best of all, almost anyone can get involved in one way or another – Motus is the ultimate hands-on community science project.

Another important differentiation between automated radio telemetry and other technologies available is that the temporal precision of the data can be much greater with radio telemetry as tags can repeat their signals as quickly as every 2 seconds. This extremely high temporal precision can allow for exceptionally detailed examinations of an animals behavior, movement patterns, direction and speed of flight.

The selection of specific tag type will largely depend on the spatial temporal scale of your study as well as your study species and geography.

## Deploying Tags in the Motus Network

The study location may largely determine what type of data you can expect, and which tags to use. When setting up your study, it’s important to consider how your tags may be detected by receivers in your area of interest. One tactic employed by the [Northeast Motus Collaboration](https://www.northeastmotus.com/) is to build a receiver ‘fence’ over a geographic area such that any tagged animal passing through it will get detected. In Ontario, where many more stations are available, there is a grid of stations \(or series of fences\) to allow for better spatial resolution of movements. In the end, you will need to decide what works best for your region based on migratory flyways, foraging locations, your goals, funding, and the location of nearby receivers.

Go to the [receivers map](https://motus.org/data/receiversMap) to see all currently active receivers, what frequency they operate on and which type of tags they can detect. Keep in mind that these receivers have been deployed by various researchers who check their stations at different times. It’s helpful to check the ‘last data processed’ to get an idea of how often these stations get checked – you don’t want to be stuck waiting for a station you don’t own to get checked! In addition, stations that haven’t been checked in a long time \(6 months to a year\) may be in various states of disrepair so it’s also best not to rely on these stations before contacting the project manager.

## Avoiding Tag Aliasing

Aliasing can cause false detections of your tags as well as tags from other projects. Removing them usually involves additional validation steps which can be difficult and time consuming for the researcher.

### What is aliasing and how does it occur?

Aliasing is caused by multiple tags emitting a signal at the same time and overlapping. Sometimes these interacting signals can produce a pattern which matches a different tag that is not actually present. This is due to the nature of how the unique ID is encoded in the signal. However, the parameters used to define these IDs are quite stringent, making aliasing an issue only in specific conditions.

Aliasing typically occurs when there are a large number of active tags in a small area. Because of this, certain species and tagging conditions are more likely to cause aliasing due to their behaviour. For researchers studying colonial or gregarious species such as swallows, bats, and shorebirds, they should be especially aware of this problem. _We anticipate aliasing to occur in any colony where there are more than 10 active tags at once with the same burst interval and that interval is less than 20 seconds._

The important thing is to try to keep numbers low at any given tagging site. This can be done by staggering deployments, either spatially or temporally. Most aliasing is caused by tags which have the same burst rate but a different Lotek ID. That means if you have more than one burst rate in your selection of tags, you can deploy more tags at any given site with a reduced risk of aliasing. However, _do not deploy more than one tag with the same Lotek ID, even if they have different burst rates!_

### Strategic station placement

We recommend placing stations close to your tagging site, but in conditions where there is a high potential for aliasing that may become problematic. In such cases, we suggest placing the station further away from the tagging site to reduce the number of overlapping detections.

If you want to learn more, see [Tag Aliasing](tag-aliasing.md).

## Tag Types

Motus supports two types of uniquely coded radio transmitters: NanoTags™ manufactured by [Lotek Wireless Inc](http://lotek.com/), operating on frequencies 166.380 MHz \(Western Hemisphere\), 150.100 MHz \(Europe\), and 151.500 MHz \(Australia\), and LifeTag™ and PowerTags™ manufactured by [Cellular Tracking Technologies](http://www.celltracktech.com/) \(CTT\) operating on 434 MHz globally. The two tags use fundamentally different transmission and coding systems. Nanotags tags use amplitude modulation, or AM, whereas CTT tags us frequency modulation, or FM. Nanotags emit 4-bit pules that encode a unique ID in the time difference between these pulses, called Pulse-position Modulation \(PPM\). CTT use frequency-shift keying \(FSK\) which flips between two similar frequencies to encode a binary “1” or “0”, with a total of 64 of these bits per transmission.

The distribution of stations listening for either tag is not uniform, so collaborators should consult the [Motus Receiver Map](https://motus.org/data/receiversMap/) to confirm which frequency stations are operating on throughout the network. When communicating with Lotek or CTT, be sure to explicitly state that you want your tags/system to be compatible with Motus.

It is simple to outfit some Motus receivers to be dual-mode in order to “listen” for both of these tag types. We recommend that stations be configured this way whenever possible in order to support the greatest number of researchers.

There is a lot of detail about these two tags that can’t all be explored here, but the table below summarizes the major differences. [Contact Motus](https://motus.org/contact), or the tag providers above for more information.

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">
        <p><a href="https://www.lotek.com/products/nanotags/"><b>Lotek Nanotag</b></a>
        </p>
        <p>
          <img src=".gitbook/assets/lotek-nanotag.jpg" alt="Lotek Nanotag" />
        </p>
      </th>
      <th style="text-align:left">
        <p><b>Lotek Nanotag Solar</b>
        </p>
        <p>
          <img src=".gitbook/assets/lotek-nanotag-solar.jpg" alt="Lotek Nanotag Solar"
          />
        </p>
      </th>
      <th style="text-align:left">
        <p><b>CTT LifeTags</b>
        </p>
        <p>
          <img src=".gitbook/assets/ctt-lifetag.png" alt="CTT LifeTags" />
        </p>
      </th>
      <th style="text-align:left">
        <p><b>CTT PowerTags</b>
        </p>
        <p>
          <img src=".gitbook/assets/ctt-powertag.png" alt="CTT PowerTags" />
        </p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>Manufacturer</b>
      </td>
      <td style="text-align:left"><b>Lotek</b>
      </td>
      <td style="text-align:left"><b>Lotek</b>
      </td>
      <td style="text-align:left"><b>CTT</b>
      </td>
      <td style="text-align:left"><b>CTT</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Frequency</td>
      <td style="text-align:left">150.1, 151.5, or 166.380 MHz</td>
      <td style="text-align:left">150.1, 151.5, or 166.38 MHz</td>
      <td style="text-align:left">434 MHz</td>
      <td style="text-align:left">434 MHz</td>
    </tr>
    <tr>
      <td style="text-align:left">Lifespan</td>
      <td style="text-align:left">Long (20 &#x2013; 2000 d)</td>
      <td style="text-align:left">Unlimited</td>
      <td style="text-align:left">Unlimited</td>
      <td style="text-align:left">Long (180 d to yrs)</td>
    </tr>
    <tr>
      <td style="text-align:left">Daily active period</td>
      <td style="text-align:left">24/7 or alternate 12-hour on/off</td>
      <td style="text-align:left">24/7 (battery and solar powered)</td>
      <td style="text-align:left">Only in direct sunlight (solar powered)</td>
      <td style="text-align:left">24/7</td>
    </tr>
    <tr>
      <td style="text-align:left">Weight</td>
      <td style="text-align:left">0.15 g &#x2013; 3.00 g</td>
      <td style="text-align:left">1.4 g and up</td>
      <td style="text-align:left">0.44 g and up</td>
      <td style="text-align:left">0.33 g and up</td>
    </tr>
    <tr>
      <td style="text-align:left">Smallest bird (%3 body weight)</td>
      <td style="text-align:left">5.0 g</td>
      <td style="text-align:left">46.7 g</td>
      <td style="text-align:left">14.7 g</td>
      <td style="text-align:left">11.0 g</td>
    </tr>
    <tr>
      <td style="text-align:left">Possible number of unique tags</td>
      <td style="text-align:left">&gt;36,000*</td>
      <td style="text-align:left">&gt;36,000*</td>
      <td style="text-align:left">~4 billion</td>
      <td style="text-align:left">~ 4 billion</td>
    </tr>
    <tr>
      <td style="text-align:left">Burst intervals</td>
      <td style="text-align:left">~2-40 seconds</td>
      <td style="text-align:left">Similar to CTT (may diminish with power loss) [needs more information]</td>
      <td
      style="text-align:left">2 seconds (configurable)</td>
        <td style="text-align:left">Programmable: from 1 sec up</td>
    </tr>
    <tr>
      <td style="text-align:left">Current number of compatible Motus Stations</td>
      <td style="text-align:left">
        <p>900+</p>
        <p><a href="https://motus.org/data/receiversMap/">See receiver map for distribution</a>
        </p>
      </td>
      <td style="text-align:left">
        <p>90+</p>
        <p><a href="https://motus.org/data/receiversMap/">See receiver map for distribution</a>
        </p>
      </td>
      <td style="text-align:left">
        <p>79+</p>
        <p><a href="https://motus.org/data/receiversMap/">See receiver map for distribution</a>
        </p>
      </td>
      <td style="text-align:left">
        <p>79+</p>
        <p><a href="https://motus.org/data/receiversMap/">See receiver map for distribution</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Compatible with CTT Receivers</td>
      <td style="text-align:left">SensorStation with FUNcube Dongle only</td>
      <td style="text-align:left">SensorStation with FUNcube Dongle only</td>
      <td style="text-align:left">Yes</td>
      <td style="text-align:left">Yes</td>
    </tr>
    <tr>
      <td style="text-align:left">Compatible with Lotek Receivers</td>
      <td style="text-align:left">Yes</td>
      <td style="text-align:left">Yes</td>
      <td style="text-align:left">No</td>
      <td style="text-align:left">No</td>
    </tr>
    <tr>
      <td style="text-align:left">Compatible with SensorGnome Receivers</td>
      <td style="text-align:left">With FUNcube dongle only</td>
      <td style="text-align:left">With FUNcube dongle only</td>
      <td style="text-align:left">With CTT Motus Adapter only</td>
      <td style="text-align:left">With CTT Motus Adapter only</td>
    </tr>
    <tr>
      <td style="text-align:left">Price</td>
      <td style="text-align:left">~$200 USD</td>
      <td style="text-align:left">~$200 USD</td>
      <td style="text-align:left">~$200 USD</td>
      <td style="text-align:left">~$200 USD</td>
    </tr>
    <tr>
      <td style="text-align:left">Discount</td>
      <td style="text-align:left">Contact Lotek</td>
      <td style="text-align:left">Contact Lotek</td>
      <td style="text-align:left">
        <p>5% for 20+</p>
        <p>10% for 30+</p>
      </td>
      <td style="text-align:left">
        <p>5% for 20+</p>
        <p>10% for 30+</p>
      </td>
    </tr>
  </tbody>
</table>

**\* This number is calculated by multiplying the number of unique ID’s emitted by Lotek tags \(517\) with the number of unique burst intervals available \(70\). These burst intervals range from 2.3 to 39.7 seconds, which corresponds to the number of primes between 23 and 397 such that no two burst intervals overlap with one another.**

