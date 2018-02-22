# Token-based Distribution with 3Q SDN

Your content can be protected by our Token-based auth solution.
URL scheme: `https://sdn-global-streaming-cache.3qsdn.com/s/[Generated HASH]/[Timestamp]/3144/files/17/11/766971/3144-F98zkwncqTR7BMg2.ism/manifest.m3u8?format=hls&mime=mp4&source=html5`

Generate Token in PHP

```php
// token.php

function generateToken() {

$expires = time() + 216000;
$_remote_addr = '127.0.0.1'; // Remote Adress where Content gets received from
$_user_agent = ''; // User Agent
$project_key = ''; // Your private project key
$md5 = md5($expires.$secret.$_user_agent.$_remote_addr, false);

return $md5.'/'.$expires;

}
```

Generate Link

```html
https://sdn-global-streaming-cache.3qsdn.com/s/{generateToken()}/3144/files/17/11/766971/3144-F98zkwncqTR7BMg2.ism/manifest.m3u8?format=hls&mime=mp4&source=html5
```

Back to [index](../README.md).