In this workshop you have learnt various techniques you can apply when creating containers images for applications using the Python programming language.

When building images it is always best to organise everything such that the container can run as a non root user.

For the case of the Python programming language it is recommended that you use a Python virtual environment even though the container image only hosts the one application. This avoids conflicts with packages that may have been installed as part of the operating system, into the system Python installation. Using a Python virtual environment also means you can more easily avoid using the root user during builds and at runtime.

Python also imposed a few other requirements as well, such as needing to disable buffering of output from applications, ensuring that the locale is set correctly, and dealing with Python applications that do not deal with reaping of zombie process themselves.

Because of the various complexities, where possible you are encouraged to separate out as much as possible into separate base images, with your application image derived from the base image. This avoids the maintenance nightmare caused by every application image being a snowflake which replicates the same boilerplate.
