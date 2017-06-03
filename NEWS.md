# hts 6.0.0.9999

* Earo Wang took over maintenance of the package from Rob J Hyndman.
* Replaced `ChangeLog` with a `NEWS.md` file to track changes to the package.
* Used `roxygen2` to generate and manage reference. Thanks to Yihui's `Rd2roxygen` package for easy conversion.
* Enabled `pkgdown` support.
* Allowed more control of colour in `plot.gts`.

# hts 5.0 (April 2016)

* Added mint option in forecast.gts (written by Shanika Wickramasuriya)
* Allowed arbitrary ordering of bottom level time series in hts()
* Added QR decomposition if LU decomposition fails
* Bug fixes

# hts 4.5 (17 June 2015)

* Fixed bugs in accuracy.gts().
* Fixed bug in forecast.gts() detecting the right default forecasting horizon.
* Fixed bug in gts() for a gts with one grouping variable.
* Speeded up Smatrix().
* Make SparseM package as dependency.
* Better handle missing values.
* Speeded up combinef() for Alan's algorithm.
* Added 3 new algorithms to the optimally reconciled approach.
* Fixed bug in forecast.gts() when using external regressors with parallel.
* Fixed time attributes of fitted and residual series.

# hts 4.4 (22 July 2014)

* Allowed multiple seasonal objects "msts" in hts() and gts().
* Fixed bug of MASE in accuracy.gts().
* Allowed user's defined forecasting function in forecast.gts().

# hts 4.3 (10 June 2014)

* Fixed bug of the arg "include" in plot.gts, when there are not yearly data.
* Fixed bug in combinef(), when it handles a simple hierarchy with 2 levels.
* Improved arg "characters" in hts() to automate the node structure.
* Added a new arg "characters" in gts(), which will automate the grouping matrix.
* Added a new reference to combinef() man.
* Made 'sd' the default weight in forecast.gts().

# hts 4.2 (25 Mar 2014)

* Fixed Next.Generic error in accuracy.gts.
* Adjust weights = sd.

# hts 4.1 (3 Mar 2014)

* Set the default parallel processes to 2.
* Fixed three dots in parallel computing for forecast.gts.
* Speeded up the topdown approaches.

# hts 4.0 (10 Feb 2014)

* Speeded up all existing functions.
* Restructured hts function. Argument g is replaced with nodes. Added bnames and
	characters to allow custom names.
* Added argument gnames to gts function.
* Argument groups in gts function allows the gmatrix with characters.
* Added function aggts in which users can specify whatever levels they like.
* Renamed Smatrix to smatrix.
* Added summary.gts function.
* Added more arguments to forecast.gts such as keep.fitted, keep.resid, lambda,
	weights.
* When setting method = "mo" in forecasts.gts, argument level started with 0
	rather than 1.
* Import parallel package in order to support for parallel processing.
* Added more criterions to accuracy.gts function. When keep.fitted = TRUE in
	forecast.gts function, accuracy.gts can also return in-sample error measures
	at the bottom level.
* Dropped argument criterions in accuracy.gts function.
* Added argument weights to combinef function. When it's a hts object, argument
	nodes is used instead of the summing matrix.
* combinef function returns either a gts object or time series at the bottom
  level. Dropped arguments return and hierarchical.
* Argument levels in plot.gts function allows more flexibilities.

# hts 3.01 (7 May 2013)

* Added the infantgts data
* Added the vignette

# hts 3.00 (7 March 2013)

* Restructured gts objects and dropped hts objects. A flag indicates if gts is
	hierarchical.
* gts objects can now contain forecasts as well as historical data.
* Updated plot.gts function with an option to show historical data as well as
	forecasts
* Added the window.gts function
* Moved SparseM from Depends to Imports

# hts 2.02 (3 November 2011)

* Bug fixes to cope with much bigger hierarchies

# hts 2.01 (3 November 2011)

* Changed hierarchical naming convention to allow much bigger hierarchies.

# hts 2.0 (2 September 2011)

* Added grouped time series (gts) objects, and re-wrote many functions in order
	to handle them.
* hts objects are now a subset of gts objects.
* Some old hts methods have been replaced by gts methods.
* Rob J Hyndman took over maintenance of the package from Han Lin Shang