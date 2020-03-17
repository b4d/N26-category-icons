
Get all categories from old images in repo:

```
ls -1 | cut -d' ' -f2 | tail -n +2 | cut -d'-' -f3- > categories.txt
```

Download modern icons:

```
while IFS= read -r line; do wget https://cdn.number26.de/feed/categories/micro-v2-$line; done < categories.txt
```
