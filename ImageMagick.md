```
for f in `find . -name "*.jpg"`
do
    convert $f -strip -interlace Plane -gaussian-blur 0.05 -quality 85% $f.jpg
done
```
