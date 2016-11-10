Warning: This is still a work in progress.

# Running

First run:

    docker run \
      --detach=false \
      --net="host" \
      -u 1000 \
      -v ~/.docker-$base_name:/dbox -v ~/Dropbox:/dbox/Dropbox \
      dmitryrck/dropbox install-dropbox.sh

Auth:

    docker run \
      --detach=false \
      --net="host" \
      -u 1000 \
      -v ~/.docker-dropbox:/dbox -v ~/Dropbox:/dbox/Dropbox \
      dmitryrck/dropbox /dbox/.dropbox-dist/dropboxd
