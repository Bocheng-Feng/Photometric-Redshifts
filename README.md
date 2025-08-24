# Photometric-Redshifts

This is the program of using machine learning algorithms, particularly *Random Forests* (RF), to predict galaxy redshifts using *only photometric* data, and comparing the results with the published EAZY ([Brammer et al. 2008](https://iopscience.iop.org/article/10.1086/591786/meta)) template-fitting method.

Data:[ The 3D-HST HLSP](https://archive.stsci.edu/prepds/3d-hst/)

See [here](https://archive.stsci.edu/hello-universe/3d-hst) for a breif introduction.


(Supported by [2025 A3net](https://github.com/IPMUCD3/a3net_2025?tab=readme-ov-file))

**Main Conlusions**

1. RF achieves comparable precision to EAZY.
2. RF tends to slightly overestimate at low redshifts and underestimate at higher redshifts.

![Phot_redshift_scatter](/Users/fengbocheng/Projects/Photometric-Redshifts/figures/Phot_redshift_scatter.png)

More details in this [Google dock](https://archive.stsci.edu/hello-universe/3d-hst).