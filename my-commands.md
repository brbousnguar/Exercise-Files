
# reverse the order of the display
awk ' {print $2, $1} ' names.txt

# print the whole line
awk ' {print $0} ' dukeofyork.txt
awk ' {print} ' dukeofyork.txt

# concatenation
awk ' {print $2 ", " $1} ' names.txt

# print the line with the number of the fields
awk ' {print NF, $0} ' dukeofyork.txt

# print the line with the 'up' word in it [regular expression]
awk '/up/{print NF, $0} ' dukeofyork.txt

# print the lines with of 6 words
awk 'NF==6{print} ' dukeofyork.txt
awk 'NF==6 ' dukeofyork.txt

# combine expresssion
awk '/up/{print "UP:", NF, $0} /down/{print "DOWN:", NF, $0} ' dukeofyork.txt
