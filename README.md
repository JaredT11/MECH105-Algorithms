# MECH105-Algorithms
These are the Algorithms that I have created for Mech105 utilizing different numerical methods.

## Homework 2_Part1
###### *Simple Electrical Circuit*

q0 = 10;

R = 60;

L = 9;

C = 0.00005;


t = linspace(0,0.8,100);


q = q0*exp((-R*t)/(2*L)).*cos(sqrt((1/(L*C))-(R/(2*L))^2)*t);


plot(q,t)

title('q vs t')

xlabel('time')

ylabel('capacitor')

grid on

hold on

q2 = q0*exp((-R*t)/(2*L)).*cos(sqrt((1/(L*.0005))-(R/(2*L))^2)*t);


plot(q2,t);

subplot(1,1,1);


## Homework 2_Part2

###### *Degradation of Aqueous Bromide*

t_exp = 10:10:60;

c_exp = [3.4 2.6 1.6 1.3 1.0 0.5];


t_func = (0:0.5:70);

c_func = (4.84*exp(1).^(-0.034*t_func));

## Homework 3

###### *Decisions*

plot(t_func,c_func,'green -');

plot(t_exp,c_exp,'red d');

xlabel('time');

ylabel('concentration');

hold on

grid on

legend on


V_whole = fprintf('v is %d\n');

h = 20;

if h == 20

V_whole = fprintf('new volume');

else 

V_whole = fprintf('no volume');

end

h = 20

rh = (12.5+(10.5/14)*(h-19));

v = ((19*12.5^(2))*pi+(1/3)*pi*(h-19)*(12.5^(2)+(12.5*rh)+rh^(2)));

## Homework 5

###### *Matrices*

function [A] = specialMatrix(n,m)

A = zeros(n,m);

A (1,:) = 1:m

A (:,1) = 1:n

for k=2:n

for j=2:m

A(k,j)=A(k-1,j)+A(k,j-1);

end

if nargin ~=2

error('need more inputs')

end

end

## Homework 6.5

###### *Binary Converter*

function [base2] = binaryConverter(base10)

nb = 2;

sum = base10;

reminder = 0;

i = 1;

base2 = 0;

while sum > 0

reminder = mod(sum,nb);

sum = floor(sum./nb);

base2(i) = reminder;

i = i+1;

end

base2 = flip(base2)

end

## Homework 11

###### *Root Finding*

g = 9.81;

mu = 0.55;

F = 150;

m = 25;

x = (66.81765);

format long

A = (mu*m*g)/(cosd(x)+ mu*sind(x));

fprintf('Hello');

plot(g)

angle = 66.81765;

## Homework 17 

###### *Linear Algebra Algorithm*

function [L, U, P] = luFactor(A)

[L, U, P] = lu(A);

end

## Homework 22

###### *Simpsons 1/3 Algorithm*

function [I] = Simpson(x, y)

if length(x) ~ =length(y)

error("Error use smae length vectors for x and y")

else

end

set =x(2)-x(1);

for k =2:length(x)

if set~=x(k)-x(k-1)

error("change to equally spaced variables")

return

else

end

n = x;

if length(x) == 2

trap = (x(n+1)-x(n))*(y(n+1)-y(n))/2;

I = simp + trap;

elseif length(x) == 3

simp = ((x(3)-x(1))/6)*(y(1)+4*y(2)+y(3))

I = simp

end

end
