---
layout: vidindex
---
# James Somerton Transcripts

> After HBomberGuy's latest video "Plagiarism and You(Tube)" I was incredibly dissapointed to hear that a creator I followed had been doing a whole bunch of plagiarism.  So, I dusted of my old Google Developer account and grabbed all the transcripts that I could get at the time of writing.  If I'm REALLY lucky then I'll also find an easy way to actually check all of these for plagiarism.  
> <span class="signature">--Project creator [TerraJRiley](https://github.com/TerraJRiley/James_Somerton_Transcripts)</span>

> We didn't find an automated and easy way to check all of the transcripts for plagiarism, and so this is a community effort, formatting and marking up the transcripts *by hand* for any and all instances of plagiarism, misinformation, and problematic takes. This project started days after HBomberGuy's video.  
> <span class="signature">--Project maintainer [Tustin2121](https://github.com/tustin2121/)</span>


Feel free to submit an issue [on the repo](https://github.com/tustin2121/James_Somerton_Transcripts) with any plagiarism found, or submit a pull request with new transcripts created.

<div class="instructions">
<div>

Contributors:
{%- assign contributors = site.data.cite | where: "contributor",true -%}
{%- for name in contributors %}
- [{{ name.name }}]({{name.link}}) - {{name.descriptive}}
{%- endfor -%}

</div>{%- unless site.data.options.hide_video_links or true -%}<div>

Video archives:
- [James Somerton Youtube (2023-12-03)](https://archive.org/details/james-somerton-youtube-2023-12-03) on the Internet Archive
- [James Somerton Public Records](https://archive.org/details/james-somerton-public-records) on the Internet Archive
- [James Somerton's videos (backup)](https://archive.org/details/james-somerton-videos-backup) on the Internet Archive
- ~~[James Somerton Archive](https://www.youtube.com/@JamesSomertonArchive/videos) on YouTube~~
- ~~[James Somerton Reuploads](https://youtube.com/@jamessomertonreuploads/videos) on YouTube~~
- ~~[Archive: James Somerton](https://youtube.com/@ArchiveJamesSomerton/videos) on YouTube~~ 

</div>{%- endunless -%}
</div>

<div class="total-score">
  <span class="plagiarized" style="width:{{ site.data.stats._global.vol.p }}%" title="{{ site.data.stats._global.vol.p }}% of James's video output was plagiarized"></span>
  <span class="misinfo" style="width:{{ site.data.stats._global.vol.m }}%" title="{{ site.data.stats._global.vol.m }}% of James's video output was misinformation"></span>
  <span class="yikes" style="width:{{ site.data.stats._global.vol.y }}%" title="{{ site.data.stats._global.vol.y }}% of James's video output was problematic takes"></span>
</div>

# Transcript Index

<div>
  <div class="video-card">
    <div class="title"><a href>Video Card Example (Links to Transcript)</a></div>
    <div class="date">Release Date</div>
    <div class="topics"><p>Topics</p><p>&amp; Media</p><p>Discussed</p></div>
    <div class="aka">
      <p>Alternate titles to videos, since James renamed videos a lot</p>
      <p>(Even outside trying to cover up all the plagiarism he did)</p>
      <p>Also includes words in (Thumbnail)s</p>
    </div>
    <div class="status">Transcript Status</div>
    <div class="score">
      <div class="plagiarized">P</div>
      <div class="misinfo">M</div>
      <div class="yikes">Y</div>
      <div class="bar">
        <span class="plagiarized" style="width:31%"></span>
        <span class="misinfo" style="width:20%"></span>
      </div>
    </div>
    {%- unless site.data.options.hide_video_links -%}
      <div class="vidlinks"><a href>Video</a> | <a href>Links</a></div>
    {%- endunless -%}
    <img class="thumbnail" src="{{ "/media/thumbs/example.webp" | relative_url }}" />
  </div>
</div>

<div class="instructions">
<div>

Score Squares:
- <span style="background-color: var(--video-box-stolen-bg); color: var(--video-box-stolen-text)">P = Number of sources plagiarized</span>
- <span style="background-color: var(--video-box-fabricated-bg); color: var(--video-box-fabricated-text)">M = Number of instances of misinformation</span>
- <span style="background-color: var(--video-box-yikes-bg); color: var(--video-box-yikes-text)">Y = Number of "Yikes!" takes, from misogyny to acephobia</span>
- The bar above the squares indicates how much of the video<br/>was plagiarized or misinformation by volume.

Transcript Statuses: 
- <span class="status alert">Missing</span> = Transcript is missing
- <span class="status alert">Superseded</span> = Transcript has been superseded
  - A "Superseded" transcript will not be filled in because  
  another transcript has taken its place. The pages will still  
  have info on thumbnails, alt names, and descriptions.
- <span class="status">Script</span> = Raw transcript data uploaded from a script
- <span class="status">Auto</span> = Raw auto-transcript
- <span class="status">Auto Script</span> = Raw AI-made transcript
- <span class="status ready">In Progress</span> = Transcript has some work done
- <span class="status complete">Finished</span> = Transcript is complete, citations needed.
  - A "Finished" transcript is fully formatted and has all the  
  information we know at the moment has been documented.  
  There's probably some major source we're missing, though.
- <span class="status complete">Complete</span> = Transcript has been formatted and highlighted.
  - A "Complete" transcript does *not* mean nothing is left to  
  be found.

</div>
<div>

Icon legend:
{% for n in site.data.info.notes -%}
- <i class="{{ n[1].icon }}"></i> - {{ n[1].desc }}
{% endfor -%}

</div>
</div>

{%  assign vids_fin = site.videos | where: 'status', 'Finished' -%}
{%- assign vids_comp = site.videos | where: 'status', 'Complete' -%}
{%- assign vids_fin = vids_fin | concat: vids_comp -%}
Finished: {{ vids_fin.size }} / {{ site.videos.size }} &nbsp; | &nbsp;  Complete: {{ vids_comp.size }} / {{ site.videos.size }} &nbsp; | &nbsp; [Other "fun" stats](extras/stats.md) &nbsp; | &nbsp; [How to read this site](instructions.md)

<div class="instructions">
  <label><input type="checkbox" id="view-old" /> Show old videos</label>
  <label><input type="checkbox" id="view-pod" /> Show podcast videos</label>
  <label><input type="checkbox" id="view-umm" /> Show meta videos</label>
  <label><input type="checkbox" id="view-new" /> Show new videos</label>
  <label><input type="checkbox" id="view-done" /> Hide incomplete</label>
</div>
<div class="video-list">

{% assign vidList = site.videos | sort: 'date' | reverse %}
{% for video in vidList %}
  {%- if video.parent -%}{%- continue -%}{%- endif -%}
  {%- include video-card video=video -%}
  
  {%- assign vid = video.id | split: '/' | last -%}
  {%- assign subList = site.videos | where: 'parent', vid | reverse -%}
  {%- if subList.size > 0 -%} 
    <div class="video-list {%- include video-filter video=video -%}">
      {%- for subVid in subList -%} 
        {%- include video-card video=subVid -%}
      {%- endfor -%}
    </div>
  {%- endif -%}
{% endfor %}

</div>

{% comment %}
Template for new videos
---
date: 2023‑11‑23
title: title
runtime: 0:00
status: Auto
aka: !!seq
  - "title"
topics: !!seq
  - "<media>"
links: !!seq
  - "https://archive.org/details/james-somerton-youtube-2023-12-03"
  - "https://archive.org/details/james-somerton-public-records"
  - "https://archive.org/details/james-somerton-videos-backup"
# description: "a video essay on...?"
notes:

cite:
  clips: !!map
  yikes: !!map
  misinformation: !!map
  plagiarized: !!map
---
{% endcomment %}
