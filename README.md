# Latex_Wriging_Toolkit
This repositories contains samples for quickstart in Latex writings.

## Tabular sample 1: simple tabular
* contains simple numbers and checkmarks
~~~
\begin{table}[htbp]
\caption{Comparison on ImageNet classification between different distillation modes and weight-initialization.}
\label{logits_feature}
\begin{center}
\begin{tabular}{cccccc}
\toprule
Initiation & Logit  & Feature &  ResNet18 &  ResNet34 &  ResNet50 \\
\toprule
 &  &  & 61.13 & 64.40 & 67.45 \\
 & \checkmark &  & 63.31 & 67.32 & 70.37 \\
 &  & \checkmark & 62.03 & 65.99 & 69.09 \\
 & \checkmark & \checkmark & \textbf{63.56} & \textbf{68.05} & \textbf{71.18} \\
\toprule
\checkmark &  &  & 65.00 & 66.57 & 66.21 \\
\checkmark & \checkmark &  & \textbf{66.11} & 67.98 & 69.45 \\
\checkmark &  & \checkmark & 64.68 & 67.92 & 69.96 \\
\checkmark & \checkmark & \checkmark & 66.09 & \textbf{70.04} & \textbf{71.71} \\
\bottomrule
\end{tabular}
\end{center}
\end{table}
~~~

## Tabular sample 2: ablation study
* contains 'multicolumn', 'multirow', 'toprule' and arraystretch
~~~
\begin{table}[h!]
\caption{Heterogeneous distillation. All models use ResNet architecture (18 denote ResNet18) to explore the influence of CNNs with different depth and performance as Teacher on SNNs performance, and match the feature map after each stage and before spike. All hyperparameters are the same.}
\centering
\renewcommand\arraystretch{1.1} % defining the line-width of rows
{\small % smaller characters
\scalebox{1.0}{ % controlling the scale of whole tabular
\begin{tabular}{lcccccc}
\toprule
\multirow{2}{*}{Dataset}& \multirow{2}{*}{Student Model} & \multicolumn{5}{c}{Teacher Model} \\ 
\cline{3-7}
 &  & 18 & 34 & 50 & 101 & 152 \\
\toprule
\multirow{3}{*}{CIFAR-100} & 18 & 77.85    & 78.13   &78.56    &78.69  &\textbf{78.83}           \\
 & 34 & ---      & 78.50    & 78.32    & \textbf{79.10}   & 78.58     \\
 & 50 & ---      & ---      & 79.58    & \textbf{79.62} &79.61           \\
\toprule
ImageNet & 50 & ---      & ---      & \textbf{71.71}    &     71.03      & 70.62     \\ 
\bottomrule
\end{tabular}
}}
\end{table}
~~~
