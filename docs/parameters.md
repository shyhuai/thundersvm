ThunderSVM Parameters
=====================
This page is for parameter specification in ThunderSVM. The parameters used in ThunderSVM are identical to LibSVM, so existing LibSVM users can easily get used to ThunderSVM.

command line options:
* -s: set the type of SVMs (default=0)
   * 0 -- C-SVC
   * 1 -- ``$ \nu $``-SVC
   * 2 -- one-class SVMs
   * 3 -- ``$ \epsilon $``-SVR
   * 4 -- ``$ \nu $``-SVR

* -t: set the type of kernel function (default=2)
   * 0 -- linear: ``$ \boldsymbol{x}_i^T \cdot \boldsymbol{x}_j $``
   * 1 -- polynomial: ``$ (\gamma \boldsymbol{x}_i^T \cdot \boldsymbol{x}_j + r)^d $``
   * 2 -- radial basis function (RBF): ``$ \exp(-\gamma ||\boldsymbol{x}_i - \boldsymbol{x}_j||^2) $``
   * 3 -- sigmoid: ``$ tanh(\gamma \boldsymbol{x}_i^T \cdot \boldsymbol{x}_j+ r) $``

* -d: set the degree in kernel function (default=3)
* -g: set ``$ gamma $`` in kernel function (default=``$ \frac{1}{\text{num_features}} $``)
* -r: set ``$ r $`` in kernel function (default=0)
* -c: set the parameter C of C-SVC, ``$ \epsilon $``-SVR, and ``$ \nu $``-SVR (default=1)
* -n: set the parameter ``$ \nu $`` of ``$ \nu $``-SVC, one-class SVM, and ``$ \nu $``-SVR (default=0.5)
* -p: set the ``$ \epsilon $`` in loss function of ``$ \epsilon $``-SVR (default=0.1)
* _-m: set cache memory size in MB (default=100)_
* -e: set tolerance of termination criterion (default=0.001)
* _-h: whether to use the shrinking heuristics, 0 or 1 (default=1)_
* -b: whether to train probabilistic SVC or SVR, 0 or 1 (default=0)
* -wi: for weighted C-SVC, set the parameter C of class i to ``$ wi \times C $`` (default=1)
* -v n: n-fold cross validation mode
* -u n: specify which gpu to use (default=0)

The options in italic are not applicable for GPUs, and the alternative optimizations are implemented with automatically setting working set size.
