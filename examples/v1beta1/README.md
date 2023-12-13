# Katib Examples

Katib is an open source project which uses Kubernetes CRD to run Automated
Machine Learning (AutoML) tasks. To know more about Katib follow the
[official guides](https://www.kubeflow.org/docs/components/katib/overview/).
Katib 是一个开源项目，它使用 Kubernetes CRD 来运行自动机器学习 (AutoML) 任务。
要了解有关 Katib 的更多信息，请遵循官方指南。

This directory contains examples of Katib Experiments in action. To install Katib on your
Kubernetes cluster check the
[setup guide](https://www.kubeflow.org/docs/components/katib/hyperparameter/#katib-setup).
You can use various [Katib interfaces](https://www.kubeflow.org/docs/components/katib/overview/#katib-interfaces)
to run these examples.
该目录包含 Katib 实验的实际示例。 要在 Kubernetes 集群上安装 Katib，请查看设置指南。 您可以使用各种 Katib 界面来运行这些示例。

For a complete description of the Katib Experiment specification follow the
[configuration guide](https://www.kubeflow.org/docs/components/katib/experiment/#configuration-spec)
有关 Katib Experiment 规范的完整描述，请遵循配置指南

## Local Cluster Example

Get started with Katib Experiments from your **local laptop** and
[Kind](https://github.com/kubernetes-sigs/kind/) cluster by following
[this example](./kind-cluster).
按照此示例，从本地笔记本电脑和 Kind 集群开始使用 Katib Experiments。

## AutoML Algorithms

The following examples show various AutoML algorithms in Katib.
以下示例展示了 Katib 中的各种 AutoML 算法。

### Hyperparameter Tuning
超参数调优

Check the [Hyperparameter Tuning](https://www.kubeflow.org/docs/components/katib/overview/#hyperparameters-and-hyperparameter-tuning)
Experiments for the following algorithms:
检查以下算法的超参数调优实验：

- [Random Search](./hp-tuning/random.yaml)

- [Grid Search](./hp-tuning/grid.yaml)

- [Bayesian Optimization](./hp-tuning/bayesian-optimization.yaml)

- [Tree of Parzen Estimators (TPE)](./hp-tuning/tpe.yaml)

- [Multivariate TPE](./hp-tuning/multivariate-tpe.yaml)

- [Covariance Matrix Adaptation Evaluation Strategy (CMA-ES)](./hp-tuning/cma-es.yaml)

- [Sobol's Quasirandom Sequence](./hp-tuning/sobol.yaml)

- [HyperBand](./hp-tuning/hyperband.yaml)

- [PBT](./hp-tuning/simple-pbt.yaml)

### Neural Architecture Search
神经架构搜索

Check the [Neural Architecture Search](https://www.kubeflow.org/docs/components/katib/overview/#neural-architecture-search)
Experiments for the following algorithms:
检查以下算法的神经架构搜索实验：

- [Efficient Neural Architecture Search (ENAS)](./nas/enas-gpu.yaml)

- [Differentiable Architecture Search (DARTS)](./nas/darts-gpu.yaml)

### Early Stopping
提前停止

Improve your Hyperparameter Tuning Experiments with the following
[Early Stopping](https://www.kubeflow.org/docs/components/katib/early-stopping/) algorithms:
使用以下早期停止算法改进您的超参数调整实验：

- [Median Stopping Rule](./early-stopping/median-stop.yaml)

## Katib Python SDK Examples

To learn more about Katib Python SDK check [this directory](./sdk).

## Resume Katib Experiments
恢复 Katib 实验

You can use different resume policies in Katib Experiments. Follow
[this guide](https://www.kubeflow.org/docs/components/katib/resume-experiment/)
to know more about it. Check the following examples:
您可以在 Katib Experiments 中使用不同的恢复策略。 请按照本指南了解更多信息。 检查以下示例：

- [Resume From Volume](./resume-experiment/from-volume-resume.yaml)

- [Resume Long Running Experiment](./resume-experiment/long-running-resume.yaml)

## Metrics Collector
指标收集器

Katib supports the various metrics collectors and metrics strategies.
Check the [official guide](https://www.kubeflow.org/docs/components/katib/experiment/#configuration-spec)
to know more about it. In this directory you can find the following examples:
Katib 支持各种指标收集器和指标策略。 查看官方指南以了解更多信息。 在此目录中您可以找到以下示例：

- [File Metrics Collector](./metrics-collector/file-metrics-collector.yaml)

- [Custom Metrics Collector](./metrics-collector/custom-metrics-collector.yaml)

- [Metrics Collection Strategy](./metrics-collector/metrics-collection-strategy.yaml)

## Trial Template
试用模板

You can specify different settings for your Trial template. To know more about it
follow [this guide](https://www.kubeflow.org/docs/components/katib/trial-template/#use-trial-template-to-submit-experiment).
Check the following examples:
您可以为试用模板指定不同的设置。 要了解更多信息，请遵循本指南。 检查以下示例：

- [Trial with ConfigMap Source](./trial-template/trial-configmap-source.yaml)

- [Trial with Metadata Substitution](./trial-template/trial-metadata-substitution.yaml)

## Trial Images

Check the following images for the Trial containers:

- [Tensorflow MNIST with summaries](./trial-images/tf-mnist-with-summaries)

- [MXNet MNIST](./trial-images/mxnet-mnist)

- [PyTorch MNIST](./trial-images/pytorch-mnist)

- [ENAS Keras CNN CIFAR-10](./trial-images/enas-cnn-cifar10)

- [DARTS PyTorch CNN CIFAR-10](./trial-images/darts-cnn-cifar10)

- [PBT proof of concept](./trial-images/simple-pbt)

## Katib with Kubeflow Training Operator

Katib has out of the box support for the [Kubeflow Training Operators](https://github.com/kubeflow/training-operator) to
perform Trial's [Worker job](https://www.kubeflow.org/docs/components/katib/overview/#trial).
Check the following examples for the various distributed operators:
Katib 为 Kubeflow Training Operators 提供开箱即用的支持，以执行 Trial 的 Worker 工作。 检查以下各种分布式运算符的示例：

- [TFJob MNIST with summaries](./kubeflow-training-operator/tfjob-mnist-with-summaries.yaml)

- [PyTorchJob MNIST](./kubeflow-training-operator/pytorchjob-mnist.yaml)

- [MXJob BytePS](./kubeflow-training-operator/mxjob-byteps.yaml)

- [XGBoostJob LightGBM](./kubeflow-training-operator/xgboostjob-lightgbm.yaml)

- [MPIJob Horovod](./kubeflow-training-operator/mpijob-horovod.yaml)

## Katib with Kubeflow Pipelines

To run Katib with [Kubeflow Pipelines](https://github.com/kubeflow/pipelines) check
[these examples](./kubeflow-pipelines).

## Katib with Argo Workflows

To know more about using [Argo Workflows](https://github.com/argoproj/argo-workflows)
in Katib check [this directory](./argo).

## Katib with Tekton Pipelines

To know more about using [Tekton Pipelines](https://github.com/tektoncd/pipeline)
in Katib check [this directory](./tekton).

## FPGA Support in Katib Experiments

You can run Katib Experiments on [FPGA](https://en.wikipedia.org/wiki/Field-programmable_gate_array)
based instances. For more information check [these examples](./fpga).
