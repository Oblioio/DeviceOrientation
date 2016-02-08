# DeviceOrientation

This file just takes all of the code from DeviceOrientationControls.js within the THREEJS examples and integrates the neccesary math from THREE's math classes. The math is trimmed down for a bit of optimization as well.

# Use

Just create a new instance of the class, pass a call back function, and the format you'd like the results in:

new Orientation(callbackFn, "YXZ");

Accepted result types are:

QUATERNION: "quaternion" or "quat"
MATRIX: "matrix" or "mat"
EULER ANGLES (use desired order): "xyz", "xzy", "yxz", "yzx", "zxy", "zyx"

If none of those options are passed the callback function will receive the alpha, beta, gamma, and orient values;
