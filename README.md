# Quiz-01
Matrix Vector Multiplication
def matVec(matrix,vector):
  """
  Variables matrix and vector will be multiplied using the defined function above. 
  The Inputs are defined:
  matrix-matrix with dimensions n x m
  vector-vector with dimension m
  The output will be the final_vector which will be the final product of the matrix and vector. 
  """
  n = len(matrix)
  m = len(vector)
  final_vector = []
  #This loop references the current row of the matrix
  for i in range(n):
    dot_product = 0
    #This loop references the corresponding integer in the vector
    for j in range(m):
        dot_product += matrix[i][j] * vector[j]
    final_vector.append(dot_product)
  #This should return the vector produced by the test matrix and vectors.
  return final_vector
#Test Case 1  
matrix = [[1,2],
          [3,4]]
vector = [5,6]
print(matVec(matrix,vector))
#Test Case 2
print(matVec(vector,matrix))
#Test Case 3
print(matVec("Texas Tech",6))
