# Segment Io Bundle
Bundle include segment.io library for analytics

include segmentio/analytics-php

## Installation

Installing the bundle via packagist is the quickest and simplest method of installing the bundle. Here are the steps:

### Step 1: Composer require

    $ php composer.phar require "farmatholin/segment-io-bundle":"dev-master"

### Step 2: Enable the bundle in the kernel

    <?php
    // app/AppKernel.php

    public function registerBundles()
    {
        $bundles = array(
            // ...
            new Farmatholin\SegmentIoBundle\SegmentIoBundle(),
            // ...
        );
    }

That's it! You are ready to use Segment.io with symfony2.

## Configuration
Required  segment write key:
```yml
# SegmentIoBundle Configuration
segment_io:
    write_key: "%your_key%"
```

## Usage
Get `segment_io.analytics` service from the service container and start using it:

```php
$analytics = $this->get('segment_io.analytics');
$analytics->page()
```

Refer to [Segment.io analytics-php library](https://github.com/segmentio/analytics-php).