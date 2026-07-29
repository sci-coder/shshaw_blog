---
title: "Electron Microscopy Art"
date: 2017-05-09
tags: ["art", "microscopy"]
summary: "Colourised electron-microscope images — black-and-white micrographs given an artistic touch."
aliases:
  - /electron-microscopy-art/
---
I am a Photoshop enthusiast. I have been adding colours to black-and-white electron-microscope images to give them an attractive look. Each pair below shows the **original micrograph** alongside my **colourised** version. For the ant, I also compare my hand-colourisation with an AI colourisation by **Google Gemini**.

These images are not mine. They are the property of Aalborg University. The images have been coloured here and published by permission of Aalborg University. The original image gallery at Aalborg is [here](http://www.nano.aau.dk/nanolab/equipment/electron-microscope-image-gallery/).

<style>
  .em-pairs { display: flex; flex-direction: column; gap: 2.5rem; margin-top: 1.5rem; }
  .em-pair figcaption.subject { font-weight: 600; margin-bottom: 0.6rem; }
  .em-cols { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
  .em-cols figure { margin: 0; }
  .em-cols img { width: 100%; height: auto; border-radius: 8px; display: block; }
  .em-cols figcaption { text-align: center; font-size: 0.85rem; opacity: 0.75; margin-top: 0.4rem; }
  .em-quad { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 1rem; }
  .em-quad figure { margin: 0; }
  .em-quad img { width: 100%; height: auto; border-radius: 8px; display: block; }
  .em-quad figcaption { text-align: center; font-size: 0.85rem; opacity: 0.75; margin-top: 0.4rem; }
  @media (max-width: 600px) { .em-cols { grid-template-columns: 1fr; } }
</style>

<div class="em-pairs">

  <figure class="em-pair">
    <figcaption class="subject">Ant — mine vs. Gemini</figcaption>
    <div class="em-quad">
      <figure><img src="ant1.jpg" alt="Ant — original micrograph"><figcaption>Original</figcaption></figure>
      <figure><img src="ant.jpg" alt="Ant — my colourisation"><figcaption>My colourisation</figcaption></figure>
      <figure><img src="ant-gemini-1.jpg" alt="Ant — colourised by Google Gemini"><figcaption>Gemini</figcaption></figure>
    </div>
  </figure>

So it seems like vision models are pretty good at segmentation of Electron microscope images now.

  <figure class="em-pair">
    <figcaption class="subject">Electrical Contacts</figcaption>
    <div class="em-cols">
      <figure><img src="contacts.jpg" alt="Contacts — original"><figcaption>Original</figcaption></figure>
      <figure><img src="contacts-2.jpg" alt="Contacts — colourised"><figcaption>Colourised</figcaption></figure>
    </div>
  </figure>

  <figure class="em-pair">
    <figcaption class="subject">Laser-Cut Tungsten Electrode</figcaption>
    <div class="em-cols">
      <figure><img src="84455_tungstenelectrodelasercut.jpg" alt="Tungsten electrode — original"><figcaption>Original</figcaption></figure>
      <figure><img src="tungstenelectrodelasercut.jpg" alt="Tungsten electrode — colourised"><figcaption>Colourised</figcaption></figure>
    </div>
  </figure>

</div>
