Linear systems are a fundamental part of linear algebra, a subject used in most modern mathematics. Computational algorithms for finding the solutions are an important part of numerical linear algebra, and play a prominent role in engineering, physics, chemistry, computer science, and economics. A system of non-linear equations can often be approximated by a linear system (see linearization), a helpful technique when making a mathematical model or computer simulation of a relatively complex system.
 
Very often, and in this article, the coefficients and solutions of the equations are constrained to be real or complex numbers, but the theory and algorithms apply to coefficients and solutions in any field. For other algebraic structures, other theories have been developed. For coefficients and solutions in an integral domain, such as the ring of integers, see Linear equation over a ring. For coefficients and solutions that are polynomials, see Grbner basis. For finding the "best" integer solutions among many, see Integer linear programming. For an example of a more exotic structure to which linear algebra can be applied, see Tropical geometry.
 
**Download File ✅ [https://eninlili.blogspot.com/?file=2A0PsC](https://eninlili.blogspot.com/?file=2A0PsC)**


 
This allows all the language and theory of *vector spaces* (or more generally, *modules*) to be brought to bear. For example, the collection of all possible linear combinations of the vectors on the left-hand side is called their *span*, and the equations have a solution just when the right-hand vector is within that span. If every vector within that span has exactly one expression as a linear combination of the given left-hand vectors, then any solution is unique. In any event, the span has a *basis* of linearly independent vectors that do guarantee exactly one expression; and the number of vectors in that basis (its *dimension*) cannot be larger than *m* or *n*, but it can be smaller. This is important because if we have *m* independent vectors a solution is guaranteed regardless of the right-hand side, and otherwise not guaranteed.
 
For a system involving two variables (*x* and *y*), each linear equation determines a line on the *xy*-plane. Because a solution to a linear system must satisfy all of the equations, the solution set is the intersection of these lines, and is hence either a line, a single point, or the empty set.
 
For three variables, each linear equation determines a plane in three-dimensional space, and the solution set is the intersection of these planes. Thus the solution set may be a plane, a line, a single point, or the empty set. For example, as three parallel planes do not have a common point, the solution set of their equations is empty; the solution set of the equations of three planes intersecting at a point is single point; if three planes pass through two points, their equations have at least two common solutions; in fact the solution set is infinite and consists in all the line passing through these points.[6]
 
In general, the behavior of a linear system is determined by the relationship between the number of equations and the number of unknowns. Here, "in general" means that a different behavior may occur for specific values of the coefficients of the equations.
 
The first system has infinitely many solutions, namely all of the points on the blue line. The second system has a single unique solution, namely the intersection of the two lines. The third system has no solutions, since the three lines share no common point.

It must be kept in mind that the pictures above show only the most common case (the general case). It is possible for a system of two equations and two unknowns to have no solution (if the two lines are parallel), or for a system of three equations and two unknowns to be solvable (if the three lines intersect at a single point).
 
The equations of a linear system are **independent** if none of the equations can be derived algebraically from the others. When the equations are independent, each equation contains new information about the variables, and removing any of the equations increases the size of the solution set. For linear equations, logical independence is the same as linear independence.
 
are not independent, because the third equation is the sum of the other two. Indeed, any one of these equations can be derived from the other two, and any one of the equations can be removed without affecting the solution set. The graphs of these equations are three lines that intersect at a single point.
 
A linear system is **inconsistent** if it has no solution, and otherwise, it is said to be **consistent**.[7] When the system is inconsistent, it is possible to derive a contradiction from the equations, that may always be rewritten as the statement 0 = 1.
 
are inconsistent. In fact, by subtracting the first equation from the second one and multiplying both sides of the result by 1/6, we get 0 = 1. The graphs of these equations on the *xy*-plane are a pair of parallel lines.
 
In general, inconsistencies occur if the left-hand sides of the equations in a system are linearly dependent, and the constant terms do not satisfy the dependence relation. A system of equations whose left-hand sides are linearly independent is always consistent.
 
Two linear systems using the same set of variables are **equivalent** if each of the equations in the second system can be derived algebraically from the equations in the first system, and vice versa. Two systems are equivalent if either both are inconsistent or each equation of each of them is a linear combination of the equations of the other one. It follows that two linear systems are equivalent if and only if they have the same solution set.
 
Each free variable gives the solution space one degree of freedom, the number of which is equal to the dimension of the solution set. For example, the solution set for the above equation is a line, since a point in the solution set can be chosen by specifying the value of the parameter *z*. An infinite solution of higher order may describe a plane, or higher-dimensional set.
 
For each variable, the denominator is the determinant of the matrix of coefficients, while the numerator is the determinant of a matrix in which one column has been replaced by the vector of constant terms.
 
Though Cramer's rule is important theoretically, it has little practical value for large matrices, since the computation of large determinants is somewhat cumbersome. (Indeed, large determinants are most easily computed using row reduction.)Further, Cramer's rule has very poor numerical properties, making it unsuitable for solving even small systems reliably, unless the operations are performed in rational arithmetic with unbounded precision.[*citation needed*]
 
as previously stated, where w \displaystyle \mathbf w  has completely dropped out of the solution, leaving only a single solution. In other cases, though, w \displaystyle \mathbf w  remains and hence an infinitude of potential values of the free parameter vector w \displaystyle \mathbf w  give an infinitude of solutions of the equation.
 
While systems of three or four equations can be readily solved by hand (see Cracovian), computers are often used for larger systems. The standard algorithm for solving a system of linear equations is based on Gaussian elimination with some modifications. Firstly, it is essential to avoid division by small numbers, which may lead to inaccurate results. This can be done by reordering the equations if necessary, a process known as *pivoting*. Secondly, the algorithm does not exactly do Gaussian elimination, but it computes the LU decomposition of the matrix *A*. This is mostly an organizational tool, but it is much quicker if one has to solve several systems with the same matrix *A* but different vectors **b**.
 
If the matrix *A* has some special structure, this can be exploited to obtain faster or more accurate algorithms. For instance, systems with a symmetric positive definite matrix can be solved twice as fast with the Cholesky decomposition. Levinson recursion is a fast method for Toeplitz matrices. Special methods exist also for matrices with many zero elements (so-called sparse matrices), which appear often in applications.
 
A completely different approach is often taken for very large systems, which would otherwise take too much time or memory. The idea is to start with an initial approximation to the solution (which does not have to be accurate at all), and to change this approximation in several steps to bring it closer to the true solution. Once the approximation is sufficiently accurate, this is taken to be the solution to the system. This leads to the class of iterative methods. For some sparse matrices, the introduction of randomness improves the speed of the iterative methods.[10] One example of an iterative method is the Jacobi method, where the matrix A \displaystyle A is split into its diagonal component D \displaystyle D and its non-diagonal component L + U \displaystyle L+U . An initial guess x ( 0 ) \displaystyle \mathbf x^(0) is used at the start of the algorithm. Each subsequent guess is computed using the iterative equation:
 
When the difference between guesses x ( k ) \displaystyle \mathbf x^(k) and x ( k + 1 ) \displaystyle \mathbf x^(k+1) is sufficiently small, the algorithm is said to have *converged* on the solution.[11]
 
These are exactly the properties required for the solution set to be a linear subspace of **R***n*. In particular, the solution set to a homogeneous system is the same as the null space of the corresponding matrix *A*.
 
The **solution set** to a system of equations will be the coordinates of the ordered pair(s) that satisfy all equations in the system. In other words, those values of x and y will make the equations true. Accordingly, when a system of equations is gra