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

Two Jupyter notebooks to set up and run the simulations and to visualize the temperature and salinity fields are in `notebook/`. 