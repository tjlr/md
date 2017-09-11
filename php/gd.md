Sprawdzenie czy plik ma nagłówki png

```php
function isPngFile($filename) {
	// check if the file exists
  	if (!file_exists($filename)) { return false; }
  	// define the array of first 8 png bytes or: array(0x89, 0x50, 0x4E, 0x47, 0x0D, 0x0A, 0x1A, 0x0A);
	$png_header = array(137, 80, 78, 71, 13, 10, 26, 10);
	$f = fopen($filename, 'r');
  	// read first 8 bytes from the file and close the resource
	$header = fread($f, 8);
	fclose($f);
  	// convert the string to an array
	$chars = preg_split('//', $header, -1, PREG_SPLIT_NO_EMPTY);
	// convert each charater to its ascii value	
  	$chars = array_map('ord', $chars);
  	// return true if there are no differences or false otherwise
	return (count(array_diff($png_header, $chars)) === 0);
}
```



Zmniejszenie liczby kolorów w pliku png

```php
function pngNNcolor($src,$dst,$clr) {
	$imSrc=imagecreatefrompng($src);
	list($w,$h)=getimagesize($src);
	$im=imagecreatetruecolor($w,$h);
	$bg=imagecolorallocatealpha($im,0,0,0,127);
	imagecolortransparent($im,$bg);
	imagefill($im,0,0,$bg);
	imagecopy($im,$imSrc,0,0,0,0,$w,$h);
	imagetruecolortopalette($im,false,$clr);
	imagesavealpha($im,true);
	imagepng($im,$dst,9);
	imagedestroy($im);
}
//przykład zmniejsza liczbę kolorów do 64
pngNNcolor($src,$dst,64);
```

