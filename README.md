# Databricks Spark Analytics Lab

Welcome to the **Databricks Spark Analytics Lab**, a repository maintained by **Sri Krishna Borra** containing hands-on Spark applications, notebooks, and machine learning examples designed to help you master Apache Spark and Databricks workflows.

You can find the source code and resources on GitHub at [https://github.com/srikrishnaborra/databricks-spark-analytics-lab](https://github.com/srikrishnaborra/databricks-spark-analytics-lab).

## Repository Structure

- **`chapter2`, `chapter3`, `chapter6`, `chapter7`**: Directories containing standalone Spark applications.
- **`notebooks`**: Interactive notebooks containing equivalents for the standalone applications as well as additional exercises.
- **`mlflow-project-example`**: An example project demonstrating integration with MLflow for tracking and managing machine learning lifecycles.
- **`databricks-datasets`**: Datasets used throughout the lab exercises.
- **`build_jars.py`**: A helper script to compile the standalone Spark applications.

## Getting Started

### Building Standalone Applications

To build all the JAR files for the standalone applications across chapters 2, 3, 6, and 7, run the following Python script from the root directory:

```bash
python build_jars.py
```

Alternatively, you can navigate to any specific chapter directory and build the JAR files individually as specified in their respective directories.

### Running Applications

To run the compiled standalone applications, make sure to include `$SPARK_HOME/bin` in your system's `$PATH` environment variable. This allows you to execute `spark-submit` directly without needing to prefix the full path.

## License

The original license file is unchanged.
