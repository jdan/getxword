## getxword

Fetches the [NYTimes Crossword](https://www.nytimes.com/crosswords) with the option to upload it to my [reMarkable 2](https://remarkable.com/) using [rmapi](https://github.com/juruen/rmapi)

### installation

You'll need to save your nytimes.com cookies to cookie.txt. I find it easiest to do this by opening a URL like https://www.nytimes.com/svc/crosswords/v2/puzzle/print/Jun1123.pdf in your browser with Chrome DevTools open, then navigating to the request -> Header -> Cookie

<img src="https://github.com/jdan/getxword/assets/287268/d89190cf-034d-44f4-9f12-bcd1d9afdf5c" width="500" alt="Chrome Devtools showing the request">

### usage

Fetch the crossword

```sh
getxword  # Outputs to a file like Jun1123.pdf
```

Fetch the crossword for a particular date (i.e. July 20, 2022)

```sh
getxword -d Jul2022  # Outputs to Jul2022.pdf
```

Open the crossword

```sh
getxword -o   # Downloads the crossword and opens it in your browser
```

Upload the crossword

```sh
getxword -d Jul2022 -u   # Uploads the PDF to your remarkable
                         # renames to 'Wednesday, July 20, 2022' on device
```
