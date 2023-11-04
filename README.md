# Shape-Area-and-Volume-Calculator-
#include <stdio.h>
//First, user will be prompted to choose which shape to process. Then the user will be asked whether to calculate the area OR the volume.
//Following this procedure, the required size information will be requested. In the last stage, 
//the calculation will be performed and the result will be presented to the user.


double rightCircularConeVolumeCalculator(int r,int h)
{
    double volume= 3.14*r*r*h/3;
    return  volume;
}
double rightCircularConeSurfaceAreaCalculator(int r,int s)
{
    double area=3.14*r*r+3.14*r*s;
    return area;
}
double sphereAreaCalculator(int r)
{
    double area=4*3.14*r*r;
    return area;
}
double sphereVolumeCalculator(int r)
{
    double volume = 4/3*3.14*r*r*r;
    return volume;
}
double cuboidVolumeCalculator(int x,int y,int z)
{
    double volume=x*y*z;
    return volume;
}
double cuboidAreaCalculator(int x,int y,int z)
{
    double area=2*(x+y+z);
    return area;
}
double tetrahedronVolumeCalculator(int x)
{
    double volume= x*x*x/6*1.41;
    return volume;
}
double terahedronAreaCalculator(int x)
{
    double area=x*x*1.7;
    return area;
}
double squarePrismVolumeCalculator(int x,int h)
{
    double volume=x*x*h;
    return volume;
}
double squarePrismAreaCalculator(int x,int h)
{
    double area=2*(x*x)+(4*x)*h;
    return area;
}
double rectangularPrismVolumeCalculator(int x,int y,int z)
{
    double volume=x*y*z;
    return volume;
}
double rectangularPrismAreaCalculator(int x,int y,int z)
{
    double area=2*(x+y+z);
    return area;
}
double triangularPrismVolumeCalculator(int x,int y,int h)
{
    double volume=x*y*h;
    return volume;
}
double  triangularPrismAreaCalculator(int x,int y,int z,int h,int L)
{
    double  area = x*h + L*(x+y+z);
    return area;
}
double ellipsoidVolumeCalculator(int x,int y,int h)
{
    double volume=4/3*3.14*x*y*h;
    return volume;
}
double ellipsoidAreaCalculator(int x,int y)
{
    double area=3.14*x*y;
    return area;
}

int main() {
    int a;
    int num;
    int r, h, s;
    int x, y, z;
    int L;

    printf("choose which shape you want to calculator\n "
           "    1. Right Circular Cone\n"
           "    2. Sphere\n"
           "    3. Cuboid\n"
           "    4. Tetrahedron\n"
           "    5. Square Prism\n"
           "    6. Rectangular Prism\n"
           "    7. Triangle Prism\n"
           "    8. Ellipsoid\n");
    scanf("%d", &num);

    switch (num) {
        case 1:
            printf(" your choice Right circular cone\n\n");
            printf("If you want to calculate volume please enter 1\n,"
                   "else calculator program  figure out area\n\n");
            scanf("%d", &a);

            if (a == 1) {

                printf("enter Right cicular cone's radius and height value please\n\n");
                scanf("%d%d", &r, &h);
                double rightCircularConeVolume = rightCircularConeVolumeCalculator(r, h);
                printf("Right cicular cone's volume is equal to %lf", rightCircularConeVolume);

            } else {
                printf("rightCircularCone's radius and slant height value please\n\n");
                scanf("%d%d", &r, &s);
                double rightCircularConeArea = rightCircularConeSurfaceAreaCalculator(r, s);
                printf("rightCircularCone's area equals %lf", rightCircularConeArea);
            }
            break;
        case 2:
            printf("your choice is Sphere\n\n");
            printf("If you want to calculate volume please enter 1\n,"
                   "else calculator program  figure out area\n\n");
            scanf("%d", &a);

            if (a == 1) {
                printf("enter sphere's r value please\n\n");
                scanf("%d", &r);
                double sphereVolume = sphereVolumeCalculator(r);
                printf("Sphere volume is equal to %lf", sphereVolume);
            } else {
                printf("enter sphere's r value please\n\n");
                scanf("%d", &r);
                double sphereArea = sphereAreaCalculator(r);
                printf("Sphere area equals to %lf", sphereArea);

            }
            break;
        case 3:

            printf(" your choice Cuboid \n\n");
            printf("If you want to calculate volume please enter 1\n,"
                   "else calculator program  figure out area\n\n");
            scanf("%d", &a);

            if (a == 1) {

                printf("enter Cuboid's length width and height value please\n\n");
                scanf("%d%d%d", &x, &y, &z);
                double cuboidVolume = cuboidVolumeCalculator(x, y, z);
                printf("Cuboid's volume is equal to %lf", cuboidVolume);

            } else {
                printf("enter cuboid's length width and height value please\n\n");
                scanf("%d%d%d", &x, &y, &z);
                double cuboidArea = cuboidAreaCalculator(x, y, z);
                printf("rightCircularCone's area equals %lf", cuboidArea);
            }
            break;
        case 4:
            printf(" your choice Tetrahedron \n\n");
            printf("If you want to calculate volume please enter 1\n,"
                   "else calculator program  figure out area\n\n");
            scanf("%d", &a);

            if (a == 1) {

                printf("enter Tetrahedron's side value please\n\n");
                scanf("%d", &x);
                double tetrahedronVolume = tetrahedronVolumeCalculator(x);
                printf("Tetrahedron's volume is equal to %lf", tetrahedronVolume);

            } else {
                printf("enter Tetrahedron's side  value please\n\n");
                scanf("%d", &x);
                double tetrahedronArea = terahedronAreaCalculator(x);
                printf("Tetrahedron's area equals %lf", tetrahedronArea);
            }

            break;
        case 5:
            printf(" your choice Square Prism \n\n");
            printf("If you want to calculate volume please enter 1\n,"
                   "else calculator program  figure out area\n\n");
            scanf("%d", &a);

            if (a == 1) {

                printf("enter Square Prism's side and height value please\n\n");
                scanf("%d%d", &x, &h);
                double squarePrismVolume = squarePrismVolumeCalculator(x, h);
                printf("Square Prism's volume is equal to %lf", squarePrismVolume);

            } else {
                printf("enter Square Prism's side and height value please\n\n");
                scanf("%d%d", &x, &h);
                double squarePrismArea = squarePrismAreaCalculator(x, h);
                printf("Square Prism's area equals %lf", squarePrismArea);
            }

            break;
        case 6:

            printf(" your choice Rectangular Prism\n\n");
            printf("If you want to calculate volume please enter 1\n,"
                   "else calculator program  figure out area\n\n");
            scanf("%d", &a);

            if (a == 1) {
                printf("enter Rectangular Prism's side length and height value please\n\n");
                scanf("%d%d%d", &x, &y, &z);
                double rectengularPrismVolume = rectangularPrismVolumeCalculator(x, y, z);
                printf("Rectangular Prism's volume is equal to %lf", rectengularPrismVolume);
            } else {
                printf("enter Rectangular Prism's side and height value please\n\n");
                scanf("%d%d%d", &x, &y, &z);
                double rectengularPrismArea = rectangularPrismAreaCalculator(x, y, z);
                printf("Rectangular Prism's area equals %lf", rectengularPrismArea);
            }
            break;
        case 7:

            printf(" your choice Triangle Prism\n\n");
            printf("If you want to calculate volume please enter 1\n,"
                   "else calculator program  figure out area\n\n");
            scanf("%d", &a);

            if (a == 1) {

                printf("enter Triangle Prism's side length and height  value please\n\n");
                scanf("%d%d%d", &x, &y, &z);
                double trianglarPrismVolume = triangularPrismVolumeCalculator(x, y, z);
                printf("Triangle Prism's volume is equal to %lf", trianglarPrismVolume);

            } else {
                printf("enter Triangle Prism's side width  and height also L value please\n\n");
                scanf("%d%d%d%d%d", &x, &y, &z, &h, &L);
                double rectengularPrismArea = triangularPrismAreaCalculator(x, y, z, h, L);
                printf("Triangle Prism  's area equals %lf", rectengularPrismArea);
            }
            break;
        default:
            printf(" your choice ellipsoid \n\n");
            printf("If you want to calculate volume please enter 1\n,"
                   "else calculator program  figure out area\n\n");
            scanf("%d", &a);

            if (a == 1) {

                printf("enter ellipsoid 's side length and height  value please\n\n");
                scanf("%d%d%d", &x, &y, &h);
                double ellipsoidVolume = ellipsoidVolumeCalculator(x, y, h);
                printf("Triangle Prism's volume is equal to %lf", ellipsoidVolume);
            } else {
                printf("enter ellipsoid's side and length value please\n\n");
                scanf("%d%d", &x, &y);
                double ellipsoidArea = ellipsoidAreaCalculator(x, y);
                printf("ellipsoid's area equals %lf", ellipsoidArea);
            }

    }

    return 0;
}
