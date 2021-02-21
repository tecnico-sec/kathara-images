Currently the sirs images are the ones in debian10.

To generate the images, just do:
```bash
cd debian10
make all
```

To push the images, make sure you are in an account with push permissions and do:
```bash
cd debian10
make all
make pushall
```


If you need to add some package, just add it to `sirsbase` and it will reflect on all the generated kathara packages.

If you push this repo, within the next day it will automatically push the base images to dockehub.

The images are synching to xtrm0/<image>.

Favor modifying files from `sirsbase` over the derived images.
