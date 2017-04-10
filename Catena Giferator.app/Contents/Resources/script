	# If no arguments are supplied
	if [ $# -eq 0 ]; then
	    echo "No arguments supplied!"
	    exit
	fi

	# If supplied file does not exist
	if [ ! -f "$1" ]; then
	    echo "File not found!"
	    exit
	fi

ffmpeg=./ffmpeg
gifsicle=./gifsicle
imageoptim=./ImageOptim.app/Contents/MacOS/ImageOptim

    $ffmpeg -y -i "$1" -vf fps=20,scale=200:-1:flags=lanczos,palettegen palette.png
	$ffmpeg -i "$1" -i palette.png -filter_complex "fps=20,scale=200:-1:flags=lanczos[x];[x][1:v] paletteuse=" temp.gif
	$gifsicle -O3 temp.gif -o ~/Desktop/output.gif
	$imageoptim ~/Desktop/output.gif
	rm temp.gif
	rm palette.png

