    >>> sd = colour.COLOURCHECKERS_SDS['ColorChecker N Ohta']['dark skin']
    >>> convert(sd, 'Spectral Distribution', 'sRGB', verbose_parameters={'describe': 'short'})

::

    ===============================================================================
    *                                                                             *
    *   [ Conversion Path ]                                                       *
    *                                                                             *
    *   "sd_to_XYZ" --> "XYZ_to_sRGB"                                             *
    *                                                                             *
    ===============================================================================


    array([ 0.45675795,  0.30986982,  0.24861924])
    >>> illuminant = colour.ILLUMINANTS_SDS['FL2']
    >>> convert(sd, 'Spectral Distribution', 'sRGB', sd_to_XYZ={'illuminant': illuminant})
    array([ 0.47924575,  0.31676968,  0.17362725])
