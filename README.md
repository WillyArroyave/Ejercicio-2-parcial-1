# Ejercicio-2-parcial-1
clf; clc;

Ts = 0.01;                 % resolicion o tiempo de muestreo 
t = -5:Ts:5;               % señal de tiempo

y1 = ustep(t,0);
y2 = ustep(1/3*t,-0.5);
yA = y1+y2;
subplot(2,2,1),plot(t,yA),title('Grafica 2-A')                     
axis([-3 3 -1 3]); 
grid; a=12;                     
xlabel('$t$','interpreter','latex','FontSize',a)
ylabel('$y(t)$','interpreter','latex','FontSize',a)

y3 = ustep(t,0);
y4 = 3*ustep(-t,3);
yB = y3+y4;
subplot(2,2,2),plot(t,yB),title('Grafica 2-B');
axis([-5 5 0 5]); 
grid; a=12;                     
xlabel('$t$','interpreter','latex','FontSize',a)
ylabel('$y(t)$','interpreter','latex','FontSize',a)

y5 = ustep(t,0);
y6 = 5*ustep(-3/5*t,1/5);
yC = y5+y6;
subplot(2,2,3),plot(t,yC),title('Grafica 2-C');
axis([-3 3 0 8]); 
grid; a=12;                     
xlabel('$t$','interpreter','latex','FontSize',a)
ylabel('$y(t)$','interpreter','latex','FontSize',a)

y7 = ustep(t,0);
y8 = 7*ustep(6*t,2);
yD = y7+y8;
subplot(2,2,4),plot(t,yD),title('Grafica 2-D');
axis([-4 4 -2 10]); 
grid; a=12;                     
xlabel('$t$','interpreter','latex','FontSize',a)
ylabel('$y(t)$','interpreter','latex','FontSize',a)

function y = ustep(t,ad)                  
N= length(t);
y = zeros(1,N);
    for i = 1:N
        if t(i)>= -ad
            y(i) = 1;
        end
    end
end
