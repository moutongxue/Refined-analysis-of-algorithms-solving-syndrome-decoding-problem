The experiments in this article, "Refined analysis of algorithms solving syndrome decoding problem", are based on the framework of CryptographicEstimators. We achieved our experimental results by creating two new files and modifying one existing file.
The two new files are:
CryptographicEstimators\cryptographic_estimators\SDEstimator\SDAlgorithms\bjmmc.py(The core experimental code of Chapter 3)
CryptographicEstimators\cryptographic_estimators\SDEstimator\SDAlgorithms\prebjmm.py(The core experimental code of Chapter 4.1)
The existing file is:
CryptographicEstimators\cryptographic_estimators\SDEstimator\SDAlgorithms\__init__.py(Linking auxiliary code)

After installing the dependent environment for SDE, the example testing method is as follows:
>>> from cryptographic_estimators.SDEstimator import SDEstimator
>>> from cryptographic_estimators.SDEstimator.SDAlgorithms import BJMMdw,BJMMpdw,BallCollision,Dumer,MayOzerov,Prange,Stern,BothMay
>>> SD = SDEstimator(n=3488, k=2720, w=64,excluded_algorithms = [BJMMdw,BJMMpdw,BallCollision,Dumer,MayOzerov,Prange,Ste
rn,BothMay] )
>>> SD.table(show_all_parameters=True, precision=3)