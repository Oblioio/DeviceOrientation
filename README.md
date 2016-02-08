# DeviceOrientation

This file just takes all of the code from DeviceOrientationControls.js within the THREEJS examples and integrates the neccesary math from THREE's math classes. The math is trimmed down for a bit of optimization as well.

# Use

The file is setup as a module which can be loaded with RequireJS, otherwise it will be attached globally as window.Orientation. To use it you create a new instance of the class passing a callback function and the format you'd like the results in:

> var orientationListener = new Orientation(callbackFn, "YXZ");

Accepted format types are:

 - **QUATERNION**: "quaternion" or "quat"
 - **MATRIX**: "matrix" or "mat"
 - **EULER ANGLES** (use desired order): "xyz", "xzy", "yxz", "yzx", "zxy", "zyx"

If none of those options are passed the callback function will receive the alpha, beta, gamma, and orient values.

When you no longer need the orientation you can destroy the instance:

> orientationListener.destroy();
