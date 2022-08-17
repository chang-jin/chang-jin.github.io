# Software Platform Lab Page

This is repository for Software Platform Lab webpage. We use Jekyll to run our Github page and refer to the repository of [Kording lab](https://github.com/KordingLab/KordingLab.github.io) for webpage sketch.

## Run the page locally using Jekyll

To run locally, follow instruction [here](https://jekyllrb.com/) to install Jekyll then run `jekyll serve` to see in `localhost:4000`. Here is a brief install guidelines.

```bash
sudo gem install jekyll
sudo gem install rouge
jekyll serve
```

## Editing the lab website

### Add posts

All the posts are located in `_posts` folder. Its arrangement is based on the date.
Each post should be written in markdown format.
You just have to state headers before writing contents: `layout`, `title`, `date`, and `author`.
`Contents` will be shown when you enter the detail page of the post.
See the following example of header:

``` markdown
---
layout: post
title: Orca was accepted to appear at OSDI 2022!
date: 2022-06-18 10:54:12.000000000 +09:00
type: post
author:
  email: bgchun@snu.ac.kr
  first_name: Byung-Gon
  last_name: Chun
---
```

### How to add posts

- **Clone the repository** You just have to clone this repository. Then, you can simply go to `_posts` and click `New file` then put some markdown file e.g. `2022-08-17-post-name.md` and start writing a post. And then, commit and push to the repo.

The changes will take approximately half a minute to render. You can see the new posts or changes on [spl.snu.ac.kr](http://spl.snu.ac.kr)!

### Add yourself

First, you should upload your picture on `assets/people/` folder.
Then, go to `_people` folder and create a markdown file with the name of `<firstname>_<lastname>.md` in the folder.
We require a few line of header for it. See the following example of header:

``` markdown
---
name: Changjin Jeong
picture: ../assets/people/changjin.jpg
email: create.jeong@snu.ac.kr
pgpkey: https://pgp.mit.edu/pks/lookup?op=get&search=0xDABB3F43B0C56EC1
position: ms
homepage: https://chang-jin.github.io
joined: 2021.3.2
---
```

If you don't have information, just remove the item.
For lab position, you can choose position from 4 classes including `postdoc`, `phd`, `ms`, and `alumni`. Position will put you into section in the `People` tab that you choose.

### Add new publications

All publications from the lab are located in `publications/index.md`. Please upload new publication on your own!

### Edit research page

All details for current research projects of the lab are located in `research/index.md`. Please update the file when there's a change!
