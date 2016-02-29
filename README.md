# corruption perceptions index 

the data is sourced from [transparency international](http://www.transparency.org/research/cpi/overview).  

> the corruption perceptions index (cpi) ranks countries/territories in terms of the degree to which corruption is perceived to exist among public officials and politicians. it draws on different assessments and business opinion surveys carried out by independent and reputable institutions. it captures information about the administrative and political aspects of corruption. broadly speaking, the surveys and assessments used to compile the index include questions relating to bribery of public officials, kickbacks in public procurement, embezzlement of public funds, and questions that probe the strength and effectiveness of public sector anti-corruption efforts.   

more info [here](http://www.transparency.org/cpi2014/in_detail).  

requires: 

1. r - rvest, xlsx   
2. java 8  
3. julia - gadfly, dataframes  

note: the scale of the cpi is 0-10 from 1998 to 2011, and 0-100 from 2012 onwards, due to an update to the methodology used to calculate the cpi in 2012.  

data in `data/` generated by:
```
$ ./acquire_data.r
```
or, for the paranoid:
```
$ torify ./acquire_data.r
```

`acquire_data.r` downloads files from transparency international, converts them to csv format, and mergesthem in `cpi.csv` file.  

**warning:** the files are not at all curated well. 
many countries are spelled different ways in each annual report, so the scripts will count them as different countries. 
