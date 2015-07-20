

```
find . -name "*.jpg" | xargs convert -strip -interlace Plane -gaussian-blur 0.05 -quality 85% 
```
