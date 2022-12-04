# Wyze Cam Merge Files

```bash
#!/bin/bash

[ -e list.txt ] && rm list.txt
for f in **/*.mp4
do
   echo "file $f" >> list.txt
done

ffmpeg -f concat -i list.txt joined-out.mp4 && rm list.txt
```
