# Instructions

1. Clone this repository somewhere. I.e.

        git clone --recursive https://github.com/LiaungYip/pcgen-docs G:/pcgen-docs/

   Note the use of the `--recursive` flag to download git sub-modules, i.e. the `themes/hugo-material-docs/` sub-module.

2. [Install Hugo](https://gohugo.io/overview/installing/), the static site generator.
3. At a command line:
  * `$ cd G:/pcgen-docs/`
  * `$ hugo --stepAnalysis --watch`
  * Wait for Hugo to finish generating the site. (Takes 20 seconds and ~ 100 MB of RAM on my machine.)
  * The full site is now generated. See `G:/pcgen-docs/public/` for the site.

# Sample command line session

    PS G:\pcgen-docs> hugo --stepAnalysis --watch
    Started building site
    Go initialization:
            598.9555ms (600.4816ms)    22.24 MB     79411 Allocs
    initialize & template prep:
            7.5076ms (608.4893ms)       0.93 MB     13998 Allocs
    load data:
            500.6µs (608.9899ms)        0.01 MB     164 Allocs
    read pages from source:
            212.1184ms (821.6104ms)    32.16 MB     356739 Allocs
    convert source:
            170.3187ms (992.9145ms)    89.18 MB     659430 Allocs
    build taxonomies:
            112.3785ms (1.1057935s)     8.20 MB     229698 Allocs
    render and write aliases:
            0 (1.1062775s)      0.00 MB     0 Allocs
    render and write taxonomies:
            1.5723244s (2.6791036s)   158.55 MB     2403400 Allocs
    render & write taxonomy lists:
            498.9µs (2.6806041s)        0.03 MB     667 Allocs
    render and write lists:
            1.6237175s (4.3043216s)    78.64 MB     1165825 Allocs
    render and write pages:
            15.880382s (20.1952137s)         2691.39 MB     50822615 Allocs
    render and write homepage:
            66.088ms (20.2618018s)      2.88 MB     54086 Allocs
    render and write Sitemap:
            142.7516ms (20.4050409s)           13.71 MB     315281 Allocs
    render and write robots.txt:
            0 (20.4055419s)     0.00 MB     21 Allocs
    0 draft content
    0 future content
    0 expired content
    1089 pages created
    0 non-page files copied
    0 paginator pages created
    0 tags created
    32 categories created
    in 19807 ms
    Watching for changes in G:\clone\pcgen-docs\content
    Press Ctrl+C to stop