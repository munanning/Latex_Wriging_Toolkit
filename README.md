# Latex_Wriging_Toolkit
This repositories contains samples for quickstart in Latex writings.


## Tabular sample 1: ablation study
* contains 'multicolumn', 'multirow', toprule and arraystretch
~~~
\begin{table}[h!]
\caption{Heterogeneous distillation. All models use ResNet architecture (18 denote ResNet18) to explore the influence of CNNs with different depth and performance as Teacher on SNNs performance, and match the feature map after each stage and before spike. All hyperparameters are the same.}
\centering
\renewcommand\arraystretch{1.1}
{\small 
\scalebox{1.0}{
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
