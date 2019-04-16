https://stackoverflow.com/questions/40207011/opencv-not-working-properly-with-python-on-linux-with-anaconda-getting-error-th

Exactly why I like virtual machines. I snapshot my working Python VM and then started trying installation options. They all failed until I found the one that didn't. I restored my working snapshot after each failure.

This is the solution that got OpenCV working for me.

conda remove opencv
conda install -c menpo opencv
pip install --upgrade pip
pip install opencv-contrib-python
