## 1.3.0

- Improved Water Quality event mean concentrations per updated sources from Barry Evans


## 1.2.1

- Restore perennial ice land use option

## 1.2.0

- Added lots of information into tables.py about all of the data sources for the values
- Improved curve numbers for TR55 (NRCS) for developed lands
- Rewrote Pitt's Small Storm Hydrology model to correctly be soil-type dependent and to use a look-up table for values instead of a polynomial derived from that look-up table
- For the new implementation of the Pitt/SSH model, numpy is now a requirement
- Improved evapotranspiration crop coefficients for all except developed lands. Developed Ki's still need to be sourced and fixed.
- Added a limit to the amount of runoff that can be converted to infiltration for infiltration-type BMP's. This is based on the amount of rainfall that lands on the BMP and an artificial ratio of contributing area to BMP area. Note that this ratio is based only on recommendations by the PA DEP and has nothing to do with the actual contributing areas for the BMPs as drawn.
- Recreated cluster housing as an independent land use rather than using numbers for developed_low.
- Rewrote all test modules to reflect all of the above changes.

## 1.1.3

- Fix bug which elevated the Green Roof BMP type storage capacity.  Aligned with provided documentation.

## 1.1.2

- Fix bug which threw an exception when runoff volume was 0 and BMPs were applied (essentially a precipitation value of 0).

## 1.1.1

- Allow infiltration to be increased during BMP modifications

## 1.1.0

- Allow rain garden, veg basin, porous pavement and green roof BMP types to reduce runoff
  over entire AoI according to an available volume for water storage per unit BMP Area

## 1.0.6

- Updated Curve Numbers for NLCD classes 21, 90 & 95 from input from Stroud Water Research
- Fixed Pitts impervious and urban grass calculations to align with published amounts
- Reduced imperviousness of `developed_high` NLCD type

## 1.0.4-1.0.5

- Update Exception types

## 1.0.3

- Removed unused code paths (`simulate_year`)
- Updated documentation
- Update correct D Soil type values for BMPs
- Update `barren_land` curve numbers to align with published model description

## 1.0.1-1.0.2

- Same as `1.0.0`, but with a valid `setup.py` version.

## 1.0.0

- Input format was changed. Strings used to run a model now align to NLCD types. A full list is provided in the readme. Other land types that were similar to NLCD types (and used these types to do calculations) were removed.
- Output strings were changed to match NLCD types.

## 0.2.2

- Same as `0.2.1`, but with a valid `setup.py` version.

## 0.2.1

- Fixes a bug in the computation of modified censuses. (https://github.com/WikiWatershed/tr-55/pull/40)

## 0.2.0

- The output format was changed. Previously, only the overall result of the calculation was given, after this change the overall result plus the sub-results for each (nlcd,soil) pair are given. (https://github.com/WikiWatershed/tr-55/pull/30)
- Some code was added to generate and compare mini-app ables. (https://github.com/WikiWatershed/tr-55/pull/31, https://github.com/WikiWatershed/tr-55/pull/38)
- Attempt to plug in the correct NLCD codes. Previously there were some "names" in the mini-app that did not have an associated NLCD code in the TR-55. (https://github.com/WikiWatershed/tr-55/pull/32)
- Changed the the format of the input expected by the code. It allows for areas that are covered by both reclassifications and BMPs. (https://github.com/WikiWatershed/tr-55/pull/35)
- Made it easier to do Pre-Columbian calculations. (https://github.com/WikiWatershed/tr-55/pull/37)

## 0.1.0

- Added simple STEP-L based water quality routines.

## 0.1.0.dev2

- Initial development release.
