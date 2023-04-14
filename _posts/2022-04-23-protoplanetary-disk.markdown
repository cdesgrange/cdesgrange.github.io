---
layout: post
title:  "Protoplanetary disks"
date:   2022-04-22 15:39:40
preview: fig/PDS_70-1.png
---

<b>Master research project</b> (5 months at MPIA, Heidelberg, Germany, under the supervision of Faustine Cantalloube and Thomas Henning)

A large variety of protoplanetary disks have been detected with the instrument VLT/SPHERE, and many of them contain substructures such as cavities, rings or spirals. <b>The origin of these substructures is still unknown. Are they caused by planets, but which are yet unseen? or by some other physical processes?</b> To date of my Master internship (Sept. 2020-Feb. 2021), only the protoplanetary disk PDS 70 has two confirmed giant proto-planets (Keppler et al., 2018; Müller et al., 2018; Haffert et al. 2019). In this research project, I investigated a sample of fifteen young disks from Asensio-Torres et al. (2021) with the primary goal to discover exoplanets which some are supposed to be detectable or close to be. 

<p align="center">
<img src="/fig/AsensioTorres2021_Fig_sketch_disk.png"  height="800">
<br> [Sketch from Asensio Torres et al. (2021) representing the sample of protoplanetary disks investigated in their paper and during this Master project. This is the scattered light appearance of the disks in near infrared.]
</p>


I applied the latest cutting-edge image post-processing in order to unveil them. Unfortunately, no highly robust candidates appear. I also looked into the morphology of the disks in near infrared through  Angular Differential Imaging (ADI, Marois et al., 2006), a yet unusual technique to post-process directly-imaged disks. Last, the application of six post-processing algorithms on a diverse sample of disks which have been imaged with various observational conditions enables me to compare their performance and robustness. The latest and more breakthrough post-processing MAYONNAISE (Pairet et al., 2021) confirms its state-of-the-art results to provide detailed disk images without distortion under good observational conditions.


<p align="center">
<img src="/fig/PDS70_details.png"  height="220">
<br> [My image processing with MAYONNAISE on the benchmark system PDS 70.]
</p>


<br>
<strong>Brief description of the principles of the Angular Differential Imaging technique and the post-processing MAYONNAISE:</strong>

MAYONNAISE (Morphological Analysis Yielding separated Objects iN Near infrAred usIng Sources Estimation) is the first processing of its kind on high-contrast imaging: it separates  both the planetary and disk components based on a morphological analysis and an inverse problem approach (Pairet et al. 2021). MAYONNAISE is based on ADI as it exploits the angular diversity between the star and the circumstellar signals in the image. ADI requires observations acquired in the “pupil-tracking“ mode, in which the circumstellar signals rotate around the star while the stellar light residuals are quasi-static. Hence the stellar light residuals can be subtracted by e.g. removing the median frame of the image sequence (see the Figure below). The higher is the angular variation in the image, the better works ADI and post-processing algorithms (such as MAYONNAISE) based on ADI.

<p align="center">
<img src="/fig/cadi_pc.png"  height="220">
<br> [Principle of the ADI technique. Credits: Gaël Chauvin]
</p>

The  technique <b>ADI is well suited to retrieve point sources, but not face-on disks</b> as the disk signal is captured within the median frame because it is spatially extended. Thus, the data suffer significantly from self-subtraction (Milli et al. 2012). To date, disks were retrieve with the technique PDI (Polarization Differential Imaging) mostly for the instruments as VLT/SPHERE or Gemini/GPI. The technique RDI (Referential Differential Imaging) has also been massively applied for other telescopes such as Hubble (Choquet et al. 2014) and is likely booming soon for SPHERE due to ongoing algorithmic development and new observing strategy available for this instrument.

Hence, one part of the originality of this Master internship was to retrieve various kind of disks imaged with SPHERE in total intensity by using ADI (and not PDI) with the most cutting-edge image processing. <b>Total intensity light images open the  perspective to  retrieve  the  total scattering  phase  function of the dust</b>, and coupling it to polarized light information,  constrain  deeply the  properties  of  the  micron-sized particles contained in the outer layer of the disk. 


In practice, <b>MAYONNAISE used two different representation basis</b>, each of one better suited to represent one of the components:

<ul>
  <li><b>point-like features as planets</b> are represented in pixel-basis as point sources,</li>

  <li><b>extended features as disks are represented in a wavelet basis</b>, and in particular the so-called shearlet basis as more appropriate for direct-imaging data as consisting in radial wavelet vectors.</li>

</ul> 

Moreover, MAYONNAISE uses an adapted function called the <b>Huberloss function</b> to describe the statistic noise. Close to the coronagraph, the noise is Laplacian as it is of high intensities, while it is Gaussian distributed far from the coronagraph as of smaller intensities (Pairet et al., 2019).

