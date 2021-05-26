# Leave-one-out-SAGA-TPS-tin
Plugin for QGIS that automatically runs the interpolation with the saga module thinplatespline (tin) and at the same time does a leave one out validation for it. As a result one gets the interpolation result and the data of the validation for all the interpolated data points.
## General Information leave one out method
The leave one method is used to validate the accuracy of interpolations. Therefor one data point is removed in each validation step. Then the interpolation is done for that subset of the input data with the same parameters. After the interpolation the interpolated value of the validation is compared to the known value of the removed data point. This residue value (difference between the calculated value and the true value of the input data) is stored in the validation text file. In the end this procedure is repeated for all the data point of the input data set. The user can use the resulting data to calculate statistic values such as the RMSE to judge the accuracy of the interpolation as well as import the data as a shapefile to see the spatial behaviour of the residues for the data set.
## Using the Plugin (for now)
* Download the repository as a zip file
* unpack the zip folder and remove the ending of the according branch so that the folder is named "leaveoneout_tpstin"
* place it in your plugin path for QGIS - usually sits under /user/appdata/roaming/qgis/qgis%version%/profiles/default/python/plugins; can also be found through QGIS by clicking settings -> user profiles -> open active profile folder
* go to your plugin repository and activate it by checking the "Leave one out SAGA TPS (Tin)" plugin
* if evreything works correctly it should sit in the processing toolbox under interpolation validation
# additional information
* advice: open the python console while running the plugin so that you can see where all temporary layers are stored - in case you wanna check on them
