#!/bin/sh
echo -n $1,
curl "https://maps.googleapis.com/maps/api/geocode/json?address=$*&sensor=false&key=PLACE_KEY_HERE" 2>/dev/null |egrep "lat|lng" |head -2|sed "s/^.*://" |sed "s///" | sed -e :a -e '$!N; s/\n/ /; ta' 
