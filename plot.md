#Python Plot for Paleo Boundary Condition

```
fig = plt.figure(figsize=[15,10])

ax = plt.axes(projection=ccrs.PlateCarree())

plot_1 = ax.contourf(TS.lon, lat, TS, cmap=cmaps.GMT_polar,
                   levels=np.arange(256, 320 , 1),
                   extend='max',
                   transform=ccrs.PlateCarree())
#ax.coastlines()

plot_0 = ax.contour(lon1,lat1, landfrac, [0.5], cmap=cmaps.gsdtol, alpha=0.5)

plt.title('surface temperature', fontsize=15)

cb = fig.colorbar(plot_1,orientation='horizontal')

plt.show()

```

Note: 1. Projection is available to adjust through Canopy.  
      2. Instead of using contourf, use contour to plot single contour for the landfrac(better to plot single contour).  
      3. You could change the colorbar of landfrac and the alpha(transparency) to make the figure better.   
      
