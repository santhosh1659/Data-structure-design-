# Data-structure-design-
#Polynomial addition
def add_polynomials(poly1, poly2):
    # Determine the maximum degree of the two polynomials
    max_degree = max(len(poly1), len(poly2))

    # Pad the polynomials with zeros to make them of equal length
    poly1 += [0] * (max_degree - len(poly1))
    poly2 += [0] * (max_degree - len(poly2))

    # Add the corresponding coefficients
    result = [coeff1 + coeff2 for coeff1, coeff2 in zip(poly1, poly2)]

    return result


# Example usage
poly1 = [2, 3, 1]  # 2x^2 + 3x + 1
poly2 = [1, -2, 2]  # x^2 - 2x + 2

result = add_polynomials(poly1, poly2)
print("Result:", result)
Result: [3, 1, 3]
