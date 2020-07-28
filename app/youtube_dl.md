```
# -*- coding: utf-8 -*-
urls = [
""
]
urls.each {|url|
	#command = "youtube-dl -f bestaudio --audio-format mp3 --audio-quality 0 --keep-video #{url}"
	command = "youtube-dl -f bestaudio --extract-audio --audio-format mp3 --audio-quality 0 --keep-video #{url}"
	puts command
	system(command)
}

```
