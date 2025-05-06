-------------------------------------------
 MASATI v2
 MAritime SATellite Imagery dataset
-------------------------------------------

This dataset provides maritime scenes of optical aerial images from visible spectrum. 
The MASATI dataset contains color images in dynamic marine environments, and it can be 
used to evaluate ship detection methods. Each image may contain one or multiple targets 
in different weather and illumination conditions. The datasets is composed of 7337 
satellite images labeled according to the following seven classes: land, coast, sea, 
ship, multi, coast-ship, and detail. In addition, labeling with the bounding box for 
the location of the vessels is also included.

For more information please go to the following web page: 

https://www.iuii.ua.es/datasets/masati/index.html


LICENSE AND ACCESS
-------------------------------------------
This dataset is shared only for non-profit research or educational purposes. If you use 
this dataset or a part of it, please respect these terms of use and reference the 
original work in which it was published. 

All data were obtained from Microsoft® Bing™ Maps. You can consult the Bing Maps terms 
of use at https://www.microsoft.com/maps/product/terms.html. 
Please read carefully the included file with the terms of use shown in Microsoft® Bing™ 
Maps. 


FILE FORMAT
-------------------------------------------
The satellite images were acquired from Bing Maps in RGB and with different sizes, as 
size is dependent on the region of interest to be registered in the image. In general, 
the average image size has a spatial resolution around 512 x 512 pixels. The images are 
stored as PNG where pixel values represent RGB colors. The distance between targets and 
the acquisition satellite has also been changed in order to obtain captures at different 
altitudes.


RELATED PUBLICATIONS (CITATION)
-------------------------------------------
Please, if you use this dataset or part of it, cite one or both of the original works in which it was published:

@Article{Gallego2018,
  AUTHOR = {Gallego, Antonio-Javier and Pertusa, Antonio and Gil, Pablo},
  TITLE = {Automatic Ship Classification from Optical Aerial Images with Convolutional Neural Networks},
  JOURNAL = {Remote Sensing},
  VOLUME = {10},
  YEAR = {2018},
  NUMBER = {4},
  ARTICLE-NUMBER = {511},
  URL = {http://www.mdpi.com/2072-4292/10/4/511},
  ISSN = {2072-4292},
  DOI = {10.3390/rs10040511}
}

@article{Alashhab2019,
  author = {Samer Alashhab, Antonio-Javier Gallego, Antonio Pertusa and Pablo Gil},
  journal = {IEEE Access},
  title = {Precise Ship Location With CNN Filter Selection From Optical Aerial Images},
  year = {2019},
  volume = {7},
  pages = {96567-96582},
  doi = {10.1109/ACCESS.2019.2929080}
}

This work was funded by the Spanish Government-Ministry of Economy, Industry and 
Competitiveness trough the projects RTC-2014-1863-8 and INAER4-14Y(IDI-20141234).





