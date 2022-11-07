# Python Plot for Paleo Boundary Condition

```
fig = plt.figure(figsize=[15,10])

ax = plt.axes(projection=ccrs.PlateCarree())

plot_1 = ax.contourf(TS.lon, lat, TS, cmap=cmaps.GMT_polar,
                   levels=np.arange(256, 320 , 1),
                   extend='max',
                   transform=ccrs.PlateCarree())

plot_0 = ax.contour(lon1,lat1, landfrac, [0.5], cmap=cmaps.gsdtol, alpha=0.5)

plt.title('surface temperature', fontsize=15)

cb = fig.colorbar(plot_1,orientation='horizontal')

plt.show()

```
# Packages
  Matplotlib, Cartopy should be enough...   
  
  cmaps is the package I used for colorbar, not that important to the code itself if you have other cmap to use.   
 
# Note:
1. Projection is available to adjust through Cartopy.  

2. Instead of using contourf, use contour to plot single contour for the landfrac(better to plot a single outline).  

3. You could change the colorbar of landfrac and the alpha(transparency) to make the figure better.    


# Figure
<img width="862" alt="Screen Shot 2022-11-07 at 4 49 21 PM" src="https://user-images.githubusercontent.com/89747610/200422627-5993cf72-89cc-4f26-b7da-05d27812ae99.png">
