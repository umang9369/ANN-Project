
---

## LaTeX Version (for Portfolio / Report)

```latex
\section{Artificial Neural Network for Iris Classification}

\subsection{Dataset}

The Iris dataset consists of 150 flower samples belonging to three species:

\begin{itemize}
\item Iris-setosa
\item Iris-versicolor
\item Iris-virginica
\end{itemize}

Each sample contains four numerical features:

\begin{itemize}
\item Sepal Length
\item Sepal Width
\item Petal Length
\item Petal Width
\end{itemize}

\begin{figure}[H]
\centering
\includegraphics[width=0.95\textwidth]{iris_dataset_preview.png}
\caption{Preview of the Iris Dataset}
\end{figure}

\subsection{Model Architecture}

The neural network architecture is:

\begin{verbatim}
Input (4)
   ↓
Dense(128, ReLU)
   ↓
Dropout(0.2)
   ↓
Dense(64, ReLU)
   ↓
Dropout(0.2)
   ↓
Dense(3, Softmax)
\end{verbatim}

\subsection{Training Performance}

\begin{figure}[H]
\centering
\includegraphics[width=0.9\textwidth]{training_curve.png}
\caption{Training and Validation Accuracy}
\end{figure}

\subsection{Results}

The model achieved:

\begin{itemize}
\item Training Accuracy $\approx 99\%$
\item Validation Accuracy $\approx 100\%$
\item Effective multiclass classification using Softmax
\item Reduced overfitting through Dropout regularization
\end{itemize}
