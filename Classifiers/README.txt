- Classifiers X curves:
classifiers X curve: 50000 total curves (25000 each NFBL and IFFL), one different curve. Uses data.csv, generated in data_gen_same_Xcurve.ipynb. Only uses X values.
classifiers X dt00001: Smaller dt used for solving the ODE system than in the one before. 50000 total curves (25000 each NFBL and IFFL), one different curve. Uses data_000001.csv, generated in data_gen_same_Xcurve dt00001.ipynb. Only uses X values. 
classifiers X curve RK4: Uses the Runge-Kutta 4th order method to solve the ODE system. 50000 total curves (25000 each NFBL and IFFL), one different curve. Uses data_RK4.csv, generated in data_gen_same_Xcurve RK4.ipynb. Only uses X values. This was to prove that the different classifiers work even when not using an adaptive step size method (that uses interpolation to get the values at the specified times).
classifiers analytical same curve: Uses the analytical solutions of the ODE system. 50000 total curves (25000 each NFBL and IFFL), one different curve.  Uses data_analytical.csv, generated indata_gen_same_Xcurve analytical.ipynb. Only uses X values.
classifiers analytical different curves: It uses 25 different curves (see curves.ipynb) with D=0.0001. 50000 total curves (25000 each NFBL and IFFL). Uses data_dif_curves_noise.csv, generated in data_gen analytical Different curves.ipynb.  Only uses X values.
classifiers analytical different curves ysum: Passes the sum of all Y values and the X curve. It uses 25 different curves (see curves.ipynb) with D=0.0001. 50000 total curves (25000 each NFBL and IFFL). Uses data_dif_curves_noise.csv, generated in data_gen analytical Different curves.ipynb.

- Noise:
classifiers noise: Solves the system using stochastic differential equations, with D=0.0001. 50000 total curves (25000 each NFBL and IFFL), one different curve. Uses data_noise.csv, generated in data_gen_same_Xcurve Noise.ipynb. Only uses X values.
classifiers noisier: D=0.001. 50000 total curves (25000 each NFBL and IFFL), one different curve. Uses data_noisier.csv, generated in data_gen_same_Xcurve Noisier.ipynb. Only uses X values.
classifiers noise D01: D=0.1. 50000 total curves (25000 each NFBL and IFFL), one different curve. Uses data_noise_D_01.csv, generated in data_gen_same_Xcurve Noisier D01. Only uses X values.
classifiers different curves noise: It uses 25 different curves (see curves.ipynb) with D=0.0001. 50000 total curves (25000 each NFBL and IFFL). Uses data_dif_curves_noise.csv, generated in data_gen Noise Different curves.ipynb. Only uses X values. 
classifiers different curves noise D001: D=0.01. 50000 total curves (25000 each NFBL and IFFL). Uses data_dif_curves_noise_D_001.csv, generated in data_gen Noise D001 Different curves.ipynb. Only uses X values. 

classifiers different curves noise ysum: Passes the sum of all Y values and the X curve, D=0.0001. It has 25 different curves. Uses data_dif_curves_noise_ysum.csv, generated in data_gen Noise Different curves Ysum.ipynb.
classifiers different curves noise D001 ysum: D=0.01. Uses data_dif_curves_noise_D_001_ysum.csv, generated in data_gen Noise D001 Different curves Ysum.ipynb.


When using the analytical version of the data generation scripts, it could be optimized to only evaluate the function in every time unit, instead of every 0.01 time units. This would reduce the number of evaluations, but since the analytical solution is fast to compute, it is not necessary.