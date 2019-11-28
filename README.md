# k2_lc
Download K2 lightcurve with bash command *wget*

First, download the download scripts of all campains; 
second, combine all the download scripts to one file; 
third, use *grep* command to grep the wget download scripts from your target's K2 id, or put your K2 ids into a file and use *grep -f* command instead; 
finally, you can change the output download scripts file to a bash shell, and run it.

## Files Discription
### lc_all_wget_compaign.sh
bash shell wget the download scripts of all campaigns from
[https://archive.stsci.edu/pub/k2/download_scripts/lightcurves/all/](https://archive.stsci.edu/pub/k2/download_scripts/lightcurves/all/)

### lc_all_wget.txt
wget download scripts for all lightcurve in all campaigns 


## 
```shell
sudo chmod 755 lc_all_wget_compaign.sh
bash ./lc_all_wget_compaign.sh
```