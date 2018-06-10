def matVec(matrix,vector):
  """
  This functions uses matrix and vector as its arguments. It then multiplies the elements of the matrix by the elements of the vector before returning it as the resulting vector.
  """
  b = []
  for i in range(0,len(matrix)):
    temporary=[]
    for j in range(0,len(vector[0])):
        s = 0
        for k in range(0,len(matrix[0])):
            s += matrix[i][k]*vector[k][j]
        temporary.append(s)
    b.append(temporary)

  return b
Testmatrix01 = [[1,2,4],[3,5,6],[8,2,2]]
Testmatrix02 = [[2],[5],[2]]
Testmatrix03 = "Squirrel Bubbles"
Testvector01 = [[1],[2],[9]]
Testvector02 = [[2,4,5],[6,5,5],[4,4,4]]
Testvector03 = 33
print(matVec(Testmatrix01,Testvector01))
"""
Returns resulting vector [[41],[67],[30]]
"""
#print(matVec(Testmatrix02,Testvector02))
"""
Returns resulting matrix [[4,8,10],[10,20,25],[4,8,10]]
since vector is 3x1 and matrix is 1x3 program uses only the first row of testvector02 and multiplies it to elements of Testmatrix02.
"""
#print(matVec(Testmatrix03,Testvector03))
"""
receives error since integer is not subscriptable to function.
"""
