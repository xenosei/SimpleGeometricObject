# SimpleGeometricObject


public class SimpleGeometricObject {
    private String color = "white";
    private boolean filled;
    private java.util.Date dateCreated;

    /** Construct a default geometric object */
    public SimpleGeometricObject() {
        dateCreated = new java.util.Date();
    }


    /** Construct a geometric object with the specified color
     12 * and filled value */
    public SimpleGeometricObject(String color, boolean filled) {
        dateCreated = new java.util.Date();
        this.color = color;
        this.filled = filled;
    }

    /** Return color */
    public String getColor() {
        return color;
    }

    /** Set a new color */
    public void setColor(String color) {
        this.color = color;
    }

    /** Return filled. Since filled is boolean,
     30 its getter method is named isFilled */
    public boolean isFilled() {
        return filled;
    }

    /** Set a new filled */
    public void setFilled(boolean filled) {
        this.filled = filled;
    }

    /** Get dateCreated */
    public java.util.Date getDateCreated() {
        return dateCreated;
    }

    /** Return a string representation of this object */
    public String toString() {
        return "created on " + dateCreated + "\ncolor: " + color +
                " and filled: " + filled;
    }
    public class CircleFromSimpleGeometricObject extends SimpleGeometricObject{ // Inner class 'CircleFromSimpleGeometricObject' may be 'static' 
        private double radius;

        public CircleFromSimpleGeometricObject() { // Constructor
            radius = 1;
        }

        public CircleFromSimpleGeometricObject(double radius) {
            this.radius = radius;
        }
        public CircleFromSimpleGeometricObject(double radius, String color, boolean filled) {
            this.radius = radius;
            setColor(color);
            setFilled(filled);
        }
        /** Return radius */
        public double getRadius() {
            return radius;
        }
        /** Set a new radius */
        public void setRadius(double radius) {
            this.radius = radius;
        }
        /** Return area */
        public double getArea() {
            return radius * radius * Math.PI;
        }
        /** Return diameter */
        public double getDiameter() {
            return 2 * radius;
        }
        /** Print the circle info */
        public void printCircle() {
            System.out.println("The circle is created " +getDateCreated() +" and the radius is " +radius);
        }
        public class RectangleFromSimpleGeometricObject extends SimpleGeometricObject {
            private double width;
            private double height;

            public  RectangleFromSimpleGeometricObject() {
            }
            public RectangleFromSimpleGeometricObject(double width, double height) {
                this.width = width;
                this.height = height;
            }
            public RectangleFromSimpleGeometricObject(double width, double height, String color, boolean filled) {
                this.width = width;
                this.height = height;
                setColor(color);
                setFilled(filled);
            }
                /** Return width */
                public double getWidth() {
                    return width;
            }
            /** Set a new width */
            public void setWidth(double width) {
                this.width = width;
            }
            /** Return height */
            public double getHeight() {
                return height;
            }
            /** Set a new height */
            public void  setHeight(double height) {
                this.height = height;
            }
        }
    }

    public static void main(String[] args) {
        // Declare objects
        SimpleGeometricObject height = new SimpleGeometricObject();
        System.out.println(height.getColor());
        CircleFromSimpleGeometricObject circle = new CircleFromSimpleGeometricObject(); // error
    }
}



