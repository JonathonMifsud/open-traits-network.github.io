## Open Traits Network Registry and Website

### What is this?

This is the registry and website for the Open Traits Network.

It uses GitHub pages and can be visible here: https://open-traits-network.github.io/

We map https://opentraits.org to this address.

This registry and website was inspired by http://github.com/OBOFoundry/OBOFoundry.github.io design (see also http://obofoundry.org) and borrows from it.

### How does it work?

The source can be found on https://github.com/open-traits-network/open-traits-network.github.io

It uses GitHub Pages/[Jekyll](https://en.wikipedia.org/wiki/Jekyll_%28software%29),
a popular static site generator.

GitHub pages [are integrated with github](https://help.github.com/articles/using-jekyll-with-pages/)
which means that the entire site can be seen on https://opentraits.org (we don't run a dedicated webserver) and https://open-traits-network.github.io . 

### I have some comments

You can use the [issue tracker](https://github.com/open-traits-network/open-traits-network.github.io/issues) but you may want to hold off til things are more stable

### I want to contribute

Please do! Anyone can fork and make PR, or [create an issue in the tracker](https://github.com/open-traits-network/open-traits-network.github.io/issues).

See [CONTRIBUTING.md](CONTRIBUTING.md)

## Repo Organization

 * [_datasets/](_datasets/)   `<-- source for trait dataset metadata (yml) and markdown for display`
    * [_datasets/leafsize.md](_datasets/leafsize.md)  `<-- one file for each datasets with yaml for metadata and markdown for display`
    * ...
 * [_members/](_members/)  `<-- source for open traits network members`
    * [_members/rachael-gallangher.md](_members/rachael-gallangher.md)  `<-- metadata (yml) and markdown for display. EDIT THIS`
    * ...
 * [_posts/](_posts) `<-- Blog posts/news`
 * [_layouts/](_layouts) `<-- Jekyll layouts`
 * [_includes/](_includes) `<-- Jekyll includes`

 ## Instructions for Registry Curators

### Add Member

Members can be added by creating a file named ```<firstname>-<lastname>.md``` in [`_members/`](_members/) with content like this:

```yml
---
id: <firstname-lastname>
name: <name>
email: <email address>
homepage: <homepage url>
lat: <latitude of primary institution>
long: <longitude of primary institution>
image: <path to image file in repo>
affiliation: <primary affiliation>
info: <short info>
github: <github user name>
---

<longer info>
```

Replace the `<placeholders>` with actual values.
The fields `id` and `name` are required, all other fields are optional.
Setting `lat` and `long` will add the member to the [map](https://opentraits.org/map).
The other fields are used to enrich the popup when the member is select on the map and for the individual member pages.
The image should be stored in [`images/member`](images/member) in ```jpg``` format using your member.id as a filename (e.g., picture for member with id ```joshua-s-madin``` has image [`images/member/joshua-s-madin.jpg`](images/member/joshua-s-madin.jpg)), if `image` is not available but `github` is set the profile picture will be used on the map.

### Add Dataset
 TODO: https://github.com/open-traits-network/open-traits-network.github.io/issues/4

## Instructions for Website developers

Consult online Jekyll docs for details. Basically you just do

   gem install jekyll

(I am currently using Jekyll 4.0.0)

You can run a local test install from the top level directory

    jekyll serve

Then open http://127.0.0.1:4000

Every commit is visible within a few minutes on: https://opentraits.org and https://open-traits-network.github.io .

You may want to work on a branch to avoid disrupting the live
site. Exact procedures for accepting changes back into master have yet
to be determined. See [CONTRIBUTING.md](CONTRIBUTING.md) for a draft.

The setup is fairly standard for Jekyll. We try and keep things minimal 
so that the site will work on github. Even if you have no knowledge of Jekyll, 
it is fairly easy to introspect what is going on if you have done much CMS work or
web development.

Basics:

 * source can be markdown or html
 * Different styles of pages go in _layouts
 * ...
