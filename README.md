# Project Title

Range Determination using Boosting

## Project Description

Determination of Minimum and Maximum Prices of 100 category items based on given conditions, using the method of Boosting for removing outliers and then finding minimum and maximum prices and also finding three most common prices using python's collection library.

### Prerequisites

IndiaMART Phase2 Dataset

 [Phase2 Dataset Link](https://drive.google.com/open?id=1WdCNbjhlZgGkVnGvfforOJhS0961MMd6)


### Boosting for Outlier Elimination

```
Boosting ensemble technique with two models has been used for outlier detection and removal.

The two models are:
1. Inter-quartile range(IQR) also called Box-Plot method
2. Isolation Forest method

Dataset is first passed through IQR model and then through Isolation forest model.
The maximum and minimum from the outlier removed data is found to get the range of price 
for a particular category based on the conditions imposed. 
```

### Category-Unit wise three most common prices


Counter function of python's Collection module is used on outlier removed data to get category-unit
wise three most common prices.
```
import collections
def mostcommon(a):
  counter=collections.Counter(a)
  l=counter.most_common(3)
  
```


### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
