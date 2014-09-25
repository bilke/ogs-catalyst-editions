## Create source tree

- Fem: `python ~/paraview/Catalyst/catalyze.py -r ~/paraview -i ~/paraview/Catalyst/Editions/Base -i ~/paraview/Catalyst/Editions/Essentials -i ~/ogs-catalyst-editions/fem -o ~/catalyst/fem`
- Fem-Python: `python ~/paraview/Catalyst/catalyze.py -r ~/paraview -i ~/paraview/Catalyst/Editions/Base -i ~/paraview/Catalyst/Editions/Essentials -i ~/ogs-catalyst-editions/fem -i ~/paraview/Catalyst/Editions/Enable-Python -o ~/catalyst/fem-python`

## Build catalyst

```bash
mkdir ~/catalyst/build-fem-python
cd ~/catalyst/build-fem-python
../fem-python/cmake.sh ../fem-python
make
```

## Create repository

```bash
cd ~/catalyst/fem
find . -name .git -exec rm {} \;
git init
git add .
git commit
```
