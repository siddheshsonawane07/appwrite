<?php

use Appwrite\Client;
use Appwrite\Services\Storage;

$client = new Client();

$client
    ->setEndpoint('https://[HOSTNAME_OR_IP]/v1') // Your API Endpoint
    ->setProject('5df5acd0d48c2') // Your project ID
    ->setKey('919c2d18fb5d4...a2ae413da83346ad2') // Your secret API key
;

$storage = new Storage($client);

$result = $storage->createFile('[BUCKET_ID]', '[FILE_ID]', new \CURLFile('/path/to/file.png', 'image/png', 'file.png'));