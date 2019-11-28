# k2_lc
Download K2 lightcurve

1. Download all the wget scripts of light curves in all campaigns from the link:
[https://archive.stsci.edu/pub/k2/download_scripts/lightcurves/all/](https://archive.stsci.edu/pub/k2/download_scripts/lightcurves/all/)  
    or run the bash shell **lc_all_wget_compaign.sh**.

    ```bash
    change the permission of bash shell lc_all_wget_compaign.sh
    >>> sudo chmod +x lc_all_wget_compaign.sh
    and run the shell
    >>> bash ./lc_all_wget_compaign.sh
    ```

    All the download script files have been downloaded in the diretory **./all**

2. Combine all the download script files, and they have already been combine to the file **lc_all_wget.txt**.
    ```bash
    >>> cat all/c*_lc_all_wget.txt > lc_all_wget.txt
    ```

3. Match your k2 id with **lc_all_wget.txt**, and run *wget* or with bash shell  
    for example, if your k2 id is 210676049, use *grep* command:
    ```bash
    >>> grep 210676049 lc_all_wget.txt
    wget -q http://archive.stsci.edu/missions/k2/lightcurves/c4/210600000/76000/ktwo210676049-c04_llc.fits
    run the wget
    >>> wget -q http://archive.stsci.edu/missions/k2/lightcurves/c4/210600000/76000/ktwo210676049-c04_llc.fits
    ```
    or, put multiple k2 ids into a file in one column, use *grep -f* command:
    ```bash
    >>> grep -f k2_ids.txt lc_all_wget.txt > download_lc.sh
    change the permission of bash shell download_lc.sh, and run it to download,
    >>> sudo chmod +x download_lc.sh
    >>> bash ./download_lc.sh
    ```