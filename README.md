# kmhd-playlist-fetcher

A little single-serving web page web page that allows browsing the daily
playlist archives of Portland's KMHD radio station, created for my brother.

https://mccutchen.github.io/kmhd-playlist-fetcher/


## Implementation details

This thing was generated entirely by ChatGPT 4o, from this initial prompt:

> Please create a simple web page titled "KMHD Playlist Fetcher" that has an
> input form at the top with a "date" field and a submit button, whose target
> is the same page.  A valid date input is in the format YYYY-MM-DD.
>
> When the page is loaded with a "date=YYYY-MM-DD" query parameter, JavaScript
> should fetch the remote URL
> https://www.kmhd.org/pf/api/v3/content/fetch/playlist?query={%22day%22%3A%222023-08-03%22},
> which will return a JSON-encoded array of objects with this format:
>
> ```json
> {
>   "_duration": 208203,
>   "_id": "693afa9f45e16652dd7ba8141e083f58",
>   "_start_time": "2023-08-03T18:57:25.000-07:00",
>   "artistName": "Mk.gee",
>   "collectionName": "Pronounced McGee",
>   "trackName": "Anabell",
>   "artistViewUrl": "https://music.apple.com/us/artist/mk-gee/1122855735?uo=4",
>   "collectionViewUrl": "https://music.apple.com/us/album/anabell/1376936989?i=1376937007&uo=4",
>   "trackViewUrl": "https://music.apple.com/us/album/anabell/1376936989?i=1376937007&uo=4",
>   "previewUrl": "https://audio-ssl.itunes.apple.com/itunes-assets/AudioPreview115/v4/a6/d6/f2/a6d6f225-414a-6f9b-85a9-5349aa10c023/mzaf_10240823319740720053.plus.aac.p.m4a",
>   "artworkUrl30": "https://is3-ssl.mzstatic.com/image/thumb/Music118/v4/a8/78/2d/a8782d0d-01d1-3fda-7601-d82d9f2924de/mk-resize.jpg/30x30bb.jpg",
>   "artworkUrl60": "https://is3-ssl.mzstatic.com/image/thumb/Music118/v4/a8/78/2d/a8782d0d-01d1-3fda-7601-d82d9f2924de/mk-resize.jpg/60x60bb.jpg",
>   "artworkUrl100": "https://is3-ssl.mzstatic.com/image/thumb/Music118/v4/a8/78/2d/a8782d0d-01d1-3fda-7601-d82d9f2924de/mk-resize.jpg/100x100bb.jpg",
>   "collectionPrice": 9.99,
>   "trackPrice": 1.29,
>   "AlbumArt": "https://is3-ssl.mzstatic.com/image/thumb/Music118/v4/a8/78/2d/a8782d0d-01d1-3fda-7601-d82d9f2924de/mk-resize.jpg/60x60bb.jpg",
>   "buy": {
>     "itunes": "https://api.composer.nprstations.org/v1/widget/itunes?artistName=Mk.gee&trackName=Anabell&collectionName=Pronounced McGee&at=10l9HX",
>     "amazon": "http://www.amazon.com/s/?search-alias=digital-music&keywords=Mk.gee+Anabell&tag=oregonpublicb-20"
>   }
> }
> ```
>
> When the URL is fetched, the JavaScript should render a table with a row for
> each object in the JSON response, where each row should include the
> _start_time in the user's local time zone, the artist, and the album.

ChatGPT produced correctly functioning code on the first pass, and then I spent
a long time refining the design of the page with further prompts. It's honestly
pretty impressive to me.

[Here's the entire transcript][transcript] that went into building this.


## License

I didn't write a single line of code here.  I honestly have no idea what kind
of license would even make sense, so, for now, there is no license.

[transcript]: https://chatgpt.com/share/fed4bc7a-8fdb-4e12-86c6-4465d36eaad8
