# Welcome to the Iguazio Data Science Platform

An initial introduction to the Iguazio Data Science Platform and the platform tutorials

- [Platform Overview](#platform-overview)
- [Data Science Workflow](#data-science-workflow)
- [The Tutorial Notebooks](#the-tutorial-notebooks)
- [Getting-Started Tutorial](#getting-started-tutorial)
- [End-to-End Use-Case Applications](#end-to-end-use-case-applications)
- [Data Ingestion and Preparation](#data-ingestion-and-preparation)
- [Additional Platform Resources](#platform-resources)
- [Miscellaneous](#misc)

<a id="platform-overview"></a>

## Platform Overview

The Iguazio Data Science Platform (**"the platform"**) is a fully integrated and secure data science platform as a service (PaaS), which simplifies development, accelerates performance, facilitates collaboration, and addresses operational challenges.
The platform incorporates the following components:

- A data science workbench that includes Jupyter Notebook, integrated analytics engines, and Python packages
- Model management with experiments tracking and automated pipeline capabilities
- Managed data and machine-learning (ML) services over a scalable Kubernetes cluster
- A real-time serverless functions framework &mdash; Nuclio
- An extremely fast and secure data layer that supports SQL, NoSQL, time-series databases, files (simple objects), and streaming
- Integration with third-party data sources such as Amazon S3, HDFS, SQL databases, and streaming or messaging protocols
- Real-time dashboards based on Grafana

<br><img src="./assets/images/igz-self-service-platform.png" alt="Self-service data science platform" width="650"/><br>

<a id="data-science-workflow"></a>

## Data Science Workflow

The platform provides a complete data science workflow in a single ready-to-use platform that includes all the required building blocks for creating data science applications from research to production:

- Collect, explore, and label data from various real-time or offline sources
- Run ML training and validation at scale over multiple CPUs and GPUs
- Deploy models and applications into production with serverless functions
- Log, monitor, and visualize all your data and services

![Data Science Workflow](./assets/images/igz-data-science-workflow.gif)

<a id="the-tutorial-notebooks"></a>

## The Tutorial Notebooks

The home directory of the platform's running-user directory (**/User/&lt;running user&gt;**) contains pre-deployed tutorial Jupyter notebooks with code samples and documentation to assist you in your development &mdash; including a [**demos**](demos/README.ipynb) directory with end-to-end use-case applications (see the next section) and a [**data-ingestion-and-preparation**](data-ingestion-and-preparation/README.ipynb) directory with documentation and examples for performing data ingestion and preparation tasks.

> **Note:**
> - To view and run the tutorials from the platform, you first need to create a Jupyter Notebook service.
> - The **welcome.ipynb** notebook and main **README.md** file provide the same introduction in different formats.

<a id="getting-started-tutorial"></a>
## Getting-Started Tutorial

Start out by running the getting-started tutorial to familiarize yourself with the platform and experience firsthand some of its main capabilities.<br>
<br>
<a href="getting-started-tutorial/getting-started-tutorial.ipynb"><img src="./assets/images/view-tutorial-button.png" alt="View tutorial"/></a>

<a id="end-to-end-use-case-applications"></a>

## End-to-End Use-Case Applications

Iguazio provides full end-to-end use-case applications (demos) that demonstrate how to use the platform and related tools to address data science requirements for different industries and implementations. These demos are available in the [**MLRun demos repository**](https://github.com/mlrun/demos).

You can get the latest demos from the GitHub repository by running the following command:


```python
# Get additional demos
!/User/get-additional-demos.sh
```

<table align="left">
    <tr>
    <th>Demo</th>
    <th></th>
    <th></th>
    <th>Description</th>
    </tr>
    <tr>
        <td><b>scikit-learn pipeline</b></td>
        <td align="center", style="min-width:45px; padding: 10px;">
            <a href="demos/scikit-learn-pipeline/sklearn-project.ipynb"><img src="./assets/images/Jupyter-Logo-32px.png" /><br>Open locally</a>
        </td>
        <td align="center", style="min-width:45px; padding: 10px;">
            <a target="_blank" href="https://github.com/mlrun/demos/blob/master/scikit-learn-pipeline/">
                <img src="./assets/images/GitHub-Mark-32px.png" /><br>View on GitHub</a>
        </td>
        <td>
            Builds a full end-to-end pipeline using <a href="https://scikit-learn.org">scikit-learn</a> and the UCI <a href="http://archive.ics.uci.edu/ml/datasets/iris">Iris data set</a>
        </td>
    </tr>
    <tr>
        <td><b>Image classification with distributed training</b></td>
        <td align="center", style="min-width:45px; padding: 10px;">
            <a href="demos/image-classification-with-distributed-training/horovod-project.ipynb"><img src="./assets/images/Jupyter-Logo-32px.png" /><br>Open locally</a>
        </td>
        <td align="center", style="min-width:45px; padding: 10px;">
            <a target="_blank" href="https://github.com/mlrun/demos/tree/master/image-classification-with-distributed-training/">
                <img src="./assets/images/GitHub-Mark-32px.png" /><br>View on GitHub</a>
        </td>
        <td>
            Implements an end-to-end image-classification solution using <a href="https://www.tensorflow.org/">TensorFlow</a> (versions 1 or 2), <a href="https://keras.io/">Keras</a>, <a href="https://eng.uber.com/horovod/">Horovod</a>, and <a href="https://nuclio.io/">Nuclio</a>
        </td>
    </tr>
    <tr>
        <td><b>Face recognition</b></td>
        <td align="center", style="min-width:45px; padding: 10px;">
            <a href="demos/realtime-face-recognition/notebooks/face-recognition.ipynb"><img src="./assets/images/Jupyter-Logo-32px.png" /><br>Open locally</a>
        </td>
        <td align="center", style="min-width:45px; padding: 10px;">
            <a target="_blank" href="https://github.com/mlrun/demos/tree/master/realtime-face-recognition/"><img src="./assets/images/GitHub-Mark-32px.png" /><br>View on GitHub</a>
        </td>
        <td>
            Real-time capture, recognition, and classification of face images over a video stream, as well as location tracking of identities using <a href="https://pytorch.org/">PyTorch</a>, Image identification and tracking using <a href="https://opencv.org/">OpenCV</a> and labeling application for tagging unidentified faces using <a href="https://www.streamlit.io/">Streamlit</a>
        </td>
    </tr>
    <tr>
        <td><b>Customer churn prediction</b></td>
        <td align="center", style="min-width:45px; padding: 10px;">
            <a href="demos/customer-churn-prediction/churn-project.ipynb"><img src="./assets/images/Jupyter-Logo-32px.png" /><br>Open locally</a>
        </td>
        <td align="center", style="min-width:45px; padding: 10px;">
            <a target="_blank" href="https://github.com/mlrun/demos/tree/master/customer-churn-prediction/"><img src="./assets/images/GitHub-Mark-32px.png" /><br>View on GitHub</a>
        </td>
        <td>
            Analyses of customer-churn data using the Kaggle <a href="https://www.kaggle.com/blastchar/telco-customer-churn" rel="nofollow">Telco Customer Churn data set</a>, model training and validation using <a href="https://xgboost.readthedocs.io/" rel="nofollow">XGBoost</a>, and model serving using real-time Nuclio serverless functions
        </td>
    </tr>
    <tr>
        <td><b>Stock trading</b></td>
        <td align="center", style="min-width:45px; padding: 10px;">
            <a href="demos/stock-analysis/project.ipynb"><img src="./assets/images/Jupyter-Logo-32px.png" /><br>Open locally</a>
        </td>
        <td align="center", style="min-width:45px; padding: 10px;">
            <a target="_blank" href="https://github.com/mlrun/demos/tree/master/stock-analysis/"><img src="./assets/images/GitHub-Mark-32px.png" /><br>View on GitHub</a>
        </td>
        <td>
            Reads stock-exchange data from an internet service into a time-series database (TSDB) and performs real-time market-sentiment analysis on specific stocks; the data is saved to a platform NoSQL table for generating reports and analyzing and visualizing the data on a Grafana dashboard
        </td>
    </tr>
    <tr>
        <td><b>Network operations with drift detection</b></td>
        <td align="center", style="min-width:45px; padding: 10px;">
            <a href="demos/network-operations/project.ipynb"><img src="./assets/images/Jupyter-Logo-32px.png" /><br>Open locally</a>
        </td>
        <td align="center", style="min-width:45px; padding: 10px;">
            <a target="_blank" href="https://github.com/mlrun/demos/tree/master/network-operations/"><img src="./assets/images/GitHub-Mark-32px.png" /><br>View on GitHub</a>
        </td>
        <td>
            Error prediction based on network device telematry. Training pipeline to create a new model, serving with streaming and concept drift to monitor the model performance
        </td>
    </tr>
    </table>

<a id="data-ingestion-and-preparation"></a>

## Data Ingestion and Preparation

The Iguazio Data Science Platform (**"the platform"**) allows storing data in any format.
The platform's multi-model data layer and related APIs provide enhanced support for working with NoSQL ("key-value"), time-series, and stream data.
Various steps of the data science life cycle (pipeline) might require different tools and frameworks for working with data, especially when it comes to the different mechanisms required during the research and development phase versus the operational production phase.
The platform features a wide set of methods for manipulating and managing data, of different formats, in each step of the data life cycle, using a variety of frameworks, tools, and APIs &mdash; such as:
- Spark SQL and DataFrames
- Spark Streaming
- Presto SQL queries
- pandas DataFrames
- Dask
- V3IO Frames Python library
- V3IO SDK
- Web APIs.

Refer to [data ingestion and preparation](./data-ingestion-and-preparation/README.ipynb) for an overview of various methods for collecting, storing, and manipulating data in the platform, and refers to sample tutorial notebooks that demonstrate how to use these methods.

<a href="data-ingestion-and-preparation/README.ipynb"><img src="./assets/images/open-data-ingestion-and-preparation-button.png" alt="Open data ingestion and preparation"/></a>

<a id="platform-resources"></a>

## Additional Platform Resources

Refer to the [MLRun documentation](https://mlrun.readthedocs.io) for more information

<a href="https://mlrun.readthedocs.io"><img src="./assets/images/open-mlrun-docs-button.png" alt="Open MLRun Documentation"/></a>

Other resources:

- [Introduction video](https://www.youtube.com/watch?v=8OmAN4wd7To)
- [In-depth platform overview](platform-overview.ipynb) with a break down of the steps for developing a full data science workflow from development to production
- [Platform components, services, and development ecosystem introduction](https://www.iguazio.com/docs/latest-release/intro/ecosystem/)
- [Iguazio platform References](https://iguazio.com/docs/latest-release/reference/)
- [nuclio-jupyter SDK](https://github.com/nuclio/nuclio-jupyter/blob/master/README.md) for creating and deploying Nuclio functions with Python and Jupyter Notebook

<a id="misc"></a>

## Miscellaneous

<a id="creating-virtual-environments-in-jupyter-notebook"></a>
### Creating Virtual Environments in Jupyter Notebook

A virtual environment is a named, isolated, working copy of Python that maintains its own files, directories, and paths so that you can work with specific versions of libraries or Python itself without affecting other Python projects.
Virtual environments make it easy to cleanly separate projects and avoid problems with different dependencies and version requirements across components.
See the [virtual-env](virtual-env.ipynb) tutorial notebook for step-by-step instructions for using conda to create your own Python virtual environments, which will appear as custom kernels in Jupyter Notebook.

<a id="update-notebooks"></a>
### Updating the Tutorial Notebooks to the Latest Version

You can use the provided **igz-tutorials-get.sh** script to update the tutorial notebooks to the latest stable version available on [GitHub](https://github.com/v3io/tutorials/).
For details, see the [**update-tutorials.ipynb**](update-tutorials.ipynb) notebook.

<a id="v3io-dir"></a>
### The v3io Directory

The **v3io** directory that you see in the file browser of the Jupyter UI displays the contents of the `v3io` data mount for browsing the platform data containers.
For information about the predefined data containers and data mounts and how to reference data in these containers, see [Platform Data Containers](data-ingestion-and-preparation/README.ipynb#platform-data-containers).

<a id="support"></a>
### Support

The Iguazio [support team](mailto:support@iguazio.com) will be happy to assist with any questions.
