# Metallicity-deviation
## calculate the *Metallicity deviation* using MANGA data



* * *
#### read data_plot surface mass density.ipynb
>calculate metallicity
>calculate mask using Marvin
>select galaxies which are late-type, non-inclined and star-forming
>* late-type: fracDeV<0.7
>* non-inclined: b/a>=0.3
>* star forming spaxels>=20 per galaxy
>
>distribution of metallicity in different global mass bin
>
>export data to TXT format file
>export data to CSV format file
>read data from a CSV format file



#### down_marvin_fits.sh
>change the value of plate_file, ifu_file and num_galaxy
>* plate_file: Path of the plate file *[~~array, size=[4675,1]~~]*
>* ifu_file: Path of the ifu file *[~~array, size=[4675,1]~~]*
>* num_galaxy: Total number of the galaxies which need to be downloaded
>* by the way, if you wanna change  VOR10 to HYB10, you need to change the URL
>
>use command such as 
>```
>chmod +x down_marvin_fits.sh&&./down_marvin_fits.sh 2>error_down.log
>```
>
>after downloading the files, confirm whether they are complete
>
> ```
>ls *gz  |  wc
>```
>you can also read the log file to look for which one missed
>
>PS. data of HYB10 is not complete, such as [8481-6103](https://lore.sdss.utah.edu/marvin/galaxy/8481-6103/)
            
             
* * *    
       
### Reference
> + [manga-firefly-v2_4_3-STELLARPOP.fits ](https://www.sdss.org/dr15/manga/manga-data/manga-firefly-value-added-catalog/)    
> + [Marvin docs: Mass-Metallicity Relation](https://sdss-marvin.readthedocs.io/en/stable/tutorials/exercises/resolved_mass_metallicity_relation_SOLUTION.html)
> + [code template](https://github.com/ljh520hw/Ancillary-code/blob/master/plot_maps.py)
