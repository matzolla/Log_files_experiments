# Log_files_experiments
A repository of log files from experiments reporting results on inference for different datasets mainly `UCF101`,`HMDB51`


\begin{table*}[ht]
\centering
\footnotesize
\caption{Comparison of different methods on multiple datasets.}
\begin{tabular}{lcccccccc|cccccc}
\toprule
\multirow{3}{*}{\textbf{Method}} 
& \multicolumn{4}{c}{\textbf{UCF101$_{raw}$}} & \multicolumn{4}{c}{\textbf{HMDB51$_{raw}$}} & \multicolumn{3}{c}{\textbf{UCF101$_{reconstruct}$}} & \multicolumn{3}{c}{\textbf{HMDB51$_{reconstruct}$}} \\
\cmidrule(lr){2-5} \cmidrule(lr){6-9} \cmidrule(lr){10-12} \cmidrule(lr){13-15}
&\textbf{$\epsilon=2$} & \multicolumn{2}{c}{\textbf{$\epsilon=5$}} & \textbf{$\epsilon=8$} 
& \textbf{$\epsilon=2$} & \multicolumn{2}{c}{\textbf{$\epsilon=5$}} & \textbf{$\epsilon=8$}
& \textbf{$\epsilon=2$} & \textbf{$\epsilon=5$} & \textbf{$\epsilon=8$}
& \textbf{$\epsilon=2$} & \textbf{$\epsilon=5$} & \textbf{$\epsilon=8$} \\
\midrule
DP-SGD\cite{abadi2016deep} &25.54$\scriptstyle{\pm0.16}$ & ~~~~64.41 &&77 & 0.555 & 0.677& &44.56& 43.6 & 70.1 & 98.8& 20.1 & 11.90 &25.8 \\
Adaclip\cite{pichapati2019adaclip} & 54.11 & ~~~~57.23 & & 66& 0.483 & & & & 36.1 & 61.2 & & 10.9 & 2.45 & 8.6 \\
MultiClip-DP\cite{luo2024differentially} & 39.65 & ~~~~50.07 & & & 0.379 & & & & 25.8 & 41.4 & & 0.78 & 0.89 & 1.76 \\
DDP-SGD\cite{du2021dynamic} & 53.13 & ~~~~56.39 & & & 0.457 & & & & 34.2 & 63.8 & & 8.6 & 6.12 & 22.1 \\
Norm-DP-SGD\cite{davody2020effect} & 55.59 & ~~~~55.94 & & & 0.456 & & & & 36.4 & 64.4 & & 13.3 & 6.89 & 22.8 \\
Raw data &55.16$\scriptstyle{\pm0.59}$ & ~~~~62.40& & & 0.531 & & & & 41.5 & 69.1 & & - & - & 55.16$\scriptstyle{\pm0.59}$\\
\toprule
Video-DPRP &55.16$\scriptstyle{\pm0.59}$ & ~~~~62.40& & & 0.531 & & & & 41.5 & 69.1 & & - & - & 55.16$\scriptstyle{\pm0.59}$\\
Video-DPRP ($3\times$ clip) & 61.52 & ~~~~63.52 & & & 0.523 & & & & 41.7 & 69.4 & & 18.6 & 11.33 & 25.4 \\
\bottomrule
\end{tabular}
\end{table*}
