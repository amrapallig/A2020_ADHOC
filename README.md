# GOTM runs for the ADC paper

Notebooks to set up the [GOTM](https://gotm.net/portfolio/) simulations with KPP and $k$-$\epsilon$ under various idealized convection conditions.
These notebooks make use of the Python tools for GOTM [gotmtool](https://github.com/qingli411/gotmtool), which is included as a submodule.
Use
```
git submodule update --init --recursive
```
to check out the submodule.

Run
```
./gotm_env_init.py
```
in `gotmtool/` and follow the steps to set up the environment for gotmtool.
Make sure to set `gotmdir_data` to the full path of the `data` folder in this repository.
An active Python environment is required.

Jupyter notebooks to set up and run the simulations and to visualize the temperature and salinity fields are in `notebook/`.

## Harcourt (2015) model in GOTM

The [Harcourt (2015)](https://doi.org/10.1175/JPO-D-14-0046.1) model is implemented in [a fork of GOTM](https://github.com/qingli411/code/tree/langmuir-h15-v6). To use it, we need to manually switch the GOTM code to that version  following the steps below after initializing the GOTM environment and checking out the GOTM source code using `gotmtool`

* Go to the GOTM code directory.
```
cd gotm/code
```

* Add new remote git repository.
```
git remote add qingli411 https://github.com/qingli411/code.git
```

* Fetch the new remote.
```
git fetch qingli411
```

* Create a local branch that track the remote branch for the Harcourt (2015) model.
```
git checkout -b langmuir-h15-v6 qingli411/langmuir-h15-v6
```

* Update the submodules for GOTM.
```
git submodule update --init --recursive
```

Now we are ready to run test cases with the Harcourt (2015) model.