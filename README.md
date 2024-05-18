# NFBL - IFFL

## Project Structure

The project is divided into two main parts:

- **SBI (Simulation Based Inference):** Contains the code used for parameter estimation using the _[sbi](https://sbi-dev.github.io/sbi/)_ library.
- **Classifiers:** Contains the code used to train the classifiers using the _[scikit-learn](https://scikit-learn.org/stable/index.html)_ library. It also includes scripts for data generation within a subfolder.

## Notes

Inside the `SBI` folder, there is a folder named `SBI old valid curves` that contain the code used previously, where there were issues in the way we validate the simulations. The code in the main folder fixes this issue and uses the _[flexible interface](https://sbi-dev.github.io/sbi/tutorial/02_flexible_interface/)_ of the library, which allows us to simulate data and append them later, which saves time (apart from other benefits).

The `SBI Flexible - Restrict and save` script uses a posterior and restricts it to the region where it is likely to return valid simulations through a trained classifier [1]. The generated X and Y curves, along with their corresponding parameters, are saved as a serialized _PyTorch_ state dictionary (`simulations_500k_restricted.pt`) that can be loaded later to train the neural density estimator. This file is not uploaded to the repository due to its size.

There is a `Dill Sessions` folder that contain the trained neural density estimators. This can be loaded using the `dill` library.
Lastly, there is a `Data` folder that contain `.csv` files with the data used to train the classifiers.

[1] https://sbi-dev.github.io/sbi/tutorial/08_restriction_estimator/