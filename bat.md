### copy all files .png with today date
```
xcopy {source-path-dir}\*.png {destination-path-dir} /D:%date:~5,2%-%date:~8,2%-%date:~0,4% /y
```
