### About

This project uses jupyter notebook which you can view [here](app.ipynb).

### Get Setup Locally

The easiest way to run this is with [docker](https://www.docker.com/products/docker-desktop) installed and either yarn or npm (which are only used to make things easier to run). After cloning or downloading and navigating to this directory, this can be run in two ways:

#### CLI

To execute the notebook directly from the command line, run:

```bash
yarn nbrun
# or
npm run nbrun
# Or, the same command, directly with docker:
docker run -it --rm -v $PWD:/home/jovyan/work --rm jupyter/datascience-notebook jupyter nbconvert --execute  work/app.ipynb
```

This will start a docker container, execute the notebook, create `output.json`, and close the docker container.

#### Interactive

**Alternatively**, to run the notebook server, i.e. to run the [notebook](app.ipynb) interactively, run:

```bash
yarn jupyter # or npm run jupyter
```

and visit [`http://localhost:8888/notebooks/work/app.ipynb`](http://localhost:8888/notebooks/work/app.ipynb) in your browser.

**Additionally**, `yarn nbconvert` can be used to convert the notebook to a normal `.py` file for easy integration into existing python applications (as long as the requirements are met)

### Data Sources

Election results data from [here](https://www.sos.ca.gov/elections/prior-elections/statewide-election-results/general-election-november-8-2016/statement-vote/) specifically [here](https://elections.cdn.sos.ca.gov/sov/2016-general/sov/17-presidential-formatted.xls)
( which seems identical to supplement.)

Census Data from [here](https://data.census.gov/cedsci/table?g=0400000US06.050000&table=S1903&tid=ACSST5Y2017.S1903&t=Income%20and%20Poverty&hidePreview=true&vintage=2017&layer=state&lastDisplayedRow=28&q=&cid=S2401_C01_001E&tp=false)
