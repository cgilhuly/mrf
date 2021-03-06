Changelog
----------
* 2020-03-14: New feature:
    Reconstruct ``task.py`` structure, add options to skip resizing images and downloading catalogs to save time when tweaking parameters. Also add auto-completion of configuration parameters if not written in the ``YAML`` file by the user. 
    Now users could indicate whether use ``wide_psf`` mode or not. 

* 2020-01-20: New features:
    Incorporate Qing Liu's wide-angle PSF of Dragonfly into MRF. Now the scattered lights from bright stars are better subtracted. Notice: one of the bottleneck of MRF now is the query of Pan-STARRS catalog from MAST server, which is typically quite slow. 

* 2019-10-27: New features:
    1. Add ``sbcontrast.py`` to calculate surface brightness limit of a given spatial scale.
    2. Add examples including self-MRF and cross-MRF.

* 2019-10-15: Version 1.0.3 released. New features:
    1. Add code to determine surface brightness detection limit
    2. Add function ``adjust_mask``, which can be a convenient tool to adjust mask size after running MRF.
    3. Minor adjustment for cross-MRF.

* 2019-09-07: Version 1.0.2 released. 
    Now users don't need to configure environmental path themselves. External IRAF files are automatically installed. This version also removes strong dependence on IRAF, while users could still using IRAF methods if they have many saturated stars and large images. Sometimes it would be wrong when using IRAF method to magnify image then using ``reproject``. If the high-res image after color correction is all NaN, please use other interpolation methods such as `lanczos` or `cubic`. We also add filter correction dictionary in ``__init__.py``.


* 2019-08-23: Version 1.0.1 released.

