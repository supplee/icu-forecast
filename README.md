# ICU Forecast
A tool which risk stratifies patients for prolonged stay on ICU admission, using data available in all modern EHR software solutions.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

You will need Python 3.7 or later and the following packages (installed via pip or conda):

```
jupyter
pandas
sklearn
tensorflow
keras
catboost
lightgbm
```

In addition to python 3.7, the notebooks presume the data will be stored in a postgresql schema.  You will need to install postgresql, mysqld, sqlite, or the SQL server of your choosing.  For instructions on how to do this, [check out the eICU installation tutorial over at PhysioNet](https://eicu-crd.mit.edu/tutorials/install_eicu_locally/).


### Installing

Once you have access to a SQL server containing the data (with schema named eicu), you will need to open the Jupyter notebooks and run the notebooks in order (labeled 1 through 10).  __Note that the first Jupyter notebook will contain sqlalchemy code to connect to your SQL server, so you must modify the address after 

## Deployment

After running the notebooks, you will have a CatBoost classifier applicable to the dataset.  For deployment, you will need to wrap the code provided with an ETL from your EMR data format to match the eICU data format.  If your institution already uses eICU, this should not be an issue.

You can pickle the CatBoost classifier to run elsewhere.  One could wrap the classifier

## Built With

* [eICU-CRD](https://physionet.org/content/eicu-crd/2.0/) - Source data (requires credentialed access)
* [Anaconda]() - Dependency Management
* [Jupyter Lab](https://www.jupyter.org) - the standard for interactive Python

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

This project will not have public releases.

## Authors

* **William W. Supplee, MD** - *Initial work* - [supplee](https://github.com/supplee)

## License

This project is licensed for free distribution only as permitted by PhysioNet.

## Acknowledgments

* Thanks to Jason Lee for excellent tutorials.
* Inspired by the work of Toby Manders MD and his Insight project.

