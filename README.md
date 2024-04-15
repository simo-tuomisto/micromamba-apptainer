# Micromamba Apptainer

This small definition file can be used to create a conda environment in an apptainer / singularity container.

## Example

Create a `environment.yml` file with all needed channels present. Name the environment `base`

```yml
name: base
channels:
  - conda-forge
dependencies:
  - python
  - numpy
```

Create an apptainer image with the bootstrapping definition.

For `apptainer`:
```console
apptainer build my_env.sif micromamba_bootstrapper.def
```

For `singularity`:
```console
singularity build my_env.sif micromamba_bootstrapper.def
```
