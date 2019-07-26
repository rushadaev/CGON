# Изменение цвета текста в зависимости от цвета фона
Всё очень просто

**public function getFontColor(){
	$hex = $this -> bgColor; //Фоновый цвет в hex, без префикса #!

	//Ращбираем 
	$r = hexdec(substr($hex,0,2));
	$g = hexdec(substr($hex,2,2));
	$b = hexdec(substr($hex,4,2));
	
	//Вычисляем сумма цветов, которая скажет нам о приближённости к черному или белому 
	if($r + $g + $b > 382)
		{
    	echo "#000000";
		}
	else
		{
		echo "#ffffff";
		}
	}
  **
