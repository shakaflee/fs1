# fs1
my first try to access github with CLI

## Github-learnnig

2022-10-23 00:16:00

As I cloned this repo to my local PC follow this [article](https://docs.github.com/en/get-started/using-git/getting-changes-from-a-remote-repository)

Now I want edit this md file so make some changes to `fetch` this change to my local repo.

2022-10-23 10:21:00

Actually it should be `pull` which combine `fetch` and `merge`.

Here is how I clone this repo to my local using Git.

1. cd to where you want locate this repo on your PC, I want it at `d:/`, so:

```
cd d:/
```

2. then clone this repo use `https` to local.

```
git clone https://github.com/shakaflee/fs1.git
```

3. then I have a directory at `d:/fs1`, that means I have done the `clone` job.

4. to try `pull` changes from remote to my local, I edit `README.md` file on Github, then:
```
cd d:/fs1
# first make sure the working dir is fs1

git pull
# this is to get romote changes to my local
```
And yes, it worked.

So far, I think a basic clone repo and get changes from remote is done, all I need to do is `git pull` to get changes in future.

Now I edit this file locally, I want this be sync with remote, what I will do is:

```
git add .
# update file on my local repo

git commit -m "update README.md"
# get a snapshot of my local repo

git push origin main
# sync local changes with remote
```
here I meet an err which is:

```
Failed to conne ct to github.com port 443
# this is what Git tells me the err.

git config --global --unset http.proxy
git config --global --unset https.proxy
# here is the answer I google and find useful.
# this is to unset proxy.
# After this I can finally push to reomoto in Git.
```

