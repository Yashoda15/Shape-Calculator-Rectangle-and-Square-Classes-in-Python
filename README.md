# Shape Calculator

## Description
This project provides Python classes to represent geometric shapes, specifically rectangles and squares. It allows for calculating key properties of the shapes, generating visual representations, and performing shape comparisons. The classes are designed to be easy to use for educational purposes or basic geometric calculations.

---

## Features
- Create rectangles and squares with customizable dimensions.
- Calculate area, perimeter, and diagonal length.
- Generate a text-based picture of the shape.
- Determine how many times one shape can fit inside another.
- Easy-to-read string representations for debugging or display.

---

## Classes

### `Rectangle`
- **Attributes**:
  - `width`: Width of the rectangle.
  - `height`: Height of the rectangle.
- **Methods**:
  - `set_width(width)`: Update the rectangle's width.
  - `set_height(height)`: Update the rectangle's height.
  - `get_area()`: Returns the area of the rectangle.
  - `get_perimeter()`: Returns the perimeter of the rectangle.
  - `get_diagonal()`: Returns the length of the diagonal.
  - `get_picture()`: Returns a string representation of the rectangle using `*`. If the shape is too large (>50), returns a warning.
  - `get_amount_inside(shape)`: Returns how many times another shape can fit inside this rectangle.
  - `__str__()`: Returns a string representation of the rectangle.

### `Square` (inherits from `Rectangle`)
- **Attributes**:
  - `side`: Side length of the square (both width and height).
- **Methods**:
  - `set_side(side)`: Updates the side length of the square.
  - Overrides `set_width()` and `set_height()` to maintain equal sides.
  - `__str__()`: Returns a string representation of the square.

---

## Usage Example

```python
from shapes import Rectangle, Square

# Rectangle
rect = Rectangle(10, 5)
print(rect.get_area())        # 50
print(rect.get_perimeter())   # 30
print(rect.get_diagonal())    # 11.180339887498949
print(rect.get_picture())

# Square
sq = Square(9)
print(sq.get_area())          # 81
sq.set_side(4)
print(sq)                     # Square(side=4)

# Check how many squares fit inside a rectangle
print(rect.get_amount_inside(sq))  # 2
