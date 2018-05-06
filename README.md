The goal of this paper is to identify novel methods for detecting anomalies in network
IP data. The data is comprised of four continuous features (source bytes, destination
bytes, source packets, destination packets) divided by their respective source port
and destination port combinations. Thus, the data is represented as a 3-dimensional
tensor T (m x n x 4), where m is the number of source ports, n is the number of
destination ports, and 4 is the number of numerical features. Each cell in T, t_ijk stores
the mean of the observations of continuous feature k between source port at index i
and destination port at index j. This paper proposes three techniques for generating
means to fill in the missing cells in T, thereby completing the tensor, so as to provide
reasonable estimates for new observations between every possible port combination.
In the context of anomaly detection, new observations between ports that do not
align closely with their corresponding estimate in T are considered anomalies. The
first technique uses a low-rank singular value decomposition algorithm for completing
individual matrix slices of the tensor. The second defines a statistical model for the
values in T and uses a Bayesian Gibbs sampling procedure to simulate missing cells
in individual matrix slices of T. Finally, the third approach extends the first and
second approaches to completing the tensor all at once, rather than with completing
individual matrices.
