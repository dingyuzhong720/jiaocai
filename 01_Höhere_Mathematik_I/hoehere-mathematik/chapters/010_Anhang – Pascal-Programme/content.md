# Anhang – Pascal-Programme

原始 PDF 第 523–532 页。

## Anhang: Pascal-Programme

```txt
program Horner(input, output);
const maxgrad = 50;
var    N, I      : integer;
        A, C      : array[0..maxgrad] of real;
        B      : real;
begin
    write('Polynomgrad = '); read(N);
    for   I:=N downto O do
        begin write(I:2,'.Koeffizient = '); read(A[I]); end;
    write('b = '); read(B);
    C[N]:=A[N];
    for I:=N-1 downto O do C[I]:=C[I+1]*B+A[I];
    writeln('f(',b,') = ',C[O]);
end.
```

```txt
program HORNERvollstaendig(input,output);
const maxgrad = 50;
var    N,I,K    : integer;
      C,A       : array[O..maxgrad]   of real;
      B       : real;
begin
    write('Polynomgrad = '); read(N);
    for I:=N downto O do
      begin write(I:2,'.Koeffizient = '); read(A[I]); end;
    write('b = '); read(B);
    for K:=0 to N do  C[K]:=A[K];
    writeln('f(x)= ');
    for K:= 0 to N-1 do
      begin C[N]:=A[N];
        for I:= N-1 downto K do C[I]:=C[I+1]*B+C[I];
        writeln (C[K],'*(x-b)^',K:2,' +');
      end;
    writeln(A[N], '*(x-b)^', N:2);
end.
```

```pascal
program NEWTONinter(input,output);
const maxgrad = 50;
var I,K,N : integer;
    P,X,H,Z,U : real;
    F : array[l..maxgrad] of real;
begin
    write('Grad = '); read(N); write('Step = '); read(H);
    write('XO = '); read(Z);
    for I:=0 to N do begin write('F',I:2,' = '); read(F[I]); end;
    for I:=1 to N do for K:=N downto I do F[K]:=(F[K]-F[K-1])/I/H;
    write('p(x) for x = '); read(X); P:=F[N]; U:=X-Z;
    for I:=N-1 downto O do P:=P*(U-I*H)+F[I];
    writeln(P);
end.
```

---

508

Anhang: Pascal-Programme

```matlab
program Bisektion(input,output);
const EPS = 1.OE-06;
var    A,B,Fa,Fb : real;

function Fn(x:real):real; begin Fn:=x*(x*x*x*x+1)+1; end;

procedure Bisect(var A,B,Fa,Fb: real);
var C,Fc :   real;
begin
    C:=(A+B)*0.5; Fc:=Fn(C);
    if Fc*Fa<=0 then begin B:=C; Fb:=Fc; end
        else begin A:=C; Fa:=Fc; end;
end;

begin
    write('A = '); read(A); writeln; write('B = '); read(B); writeln;
    Fa:=Fn(A); Fb:=Fn(B);
    if Fa*Fb>0 then begin writeln('f(a)*f(b) positiv!'); halt; end;
    while abs(A-B)>=EPS do Bisect(A,B,Fa,Fb);
    writeln('Nullstelle im Intervall:[',A,'',B,']');
end.

program NEWTONverf(input,output);
const EPS = 1.OE-5;
var    Dx,X,Xa,Fl :   real;

function F(x:real):real; begin F:=((x+1)*x+2)*x+1; end;

begin
    repeat
        begin
            Dx:=EPS;
            if abs(X)>EPS then Dx:=X*EPS;
            Fl:=F(X); X:=X+Dx; Dx:=-F(X)*Dx/(F(X)-Fl);
            X:=X+Dx; Xa:=abs(X);
            if Xa<=1 then Xa:=1;
        end;
    until (abs(Dx)<(EPS*Xa)) or (abs(F(X))<EPS);
writeln(X);
end.

program KubischeSpline(input,output);
const max = 50;
var    M,N,I,K      :integer;
        X,Y,B,C,D     :array[0..max] of real;
        R,S,Q,Z,T     :real;
begin
    write('Punktezahl = '); read(N); writeln;
    N:=N-1;
    for I:=0 to N do
        begin
            write('X',I:2,' = '); read(X[I]); writeln;
            write('Y',I:2,' = '); read(Y[I]); writeln;
```

---

Anhang: Pascal-Programme

509

```pascal
end;
M:=N-1; S:=0;
for I:=0 to M do
    begin
        D[I]:=X[I+1]-X[I]; R:=(Y[I+1]-Y[I])/D[I]; C[I]:=R-S; S:=R;
    end;
S:=0; R:=0; C[0]:=0; C[N]:=0;
for I:=1 to M do
    begin
        C[I]:=C[I]+R*C[I-1]; B[I]:=(X[I-1]-X[I+1])*2-R*S;
        S:=D[I]; R:=S/B[I];
    end;
for I:=M downto l do C[I]:=(D[I]*C[I+1]-C[I])/B[I];
for I:=1 to M do
    begin
        S:=D[I]; R:=C[I+1]-C[I]; D[I]:=R/S; C[I]:=C[I]*3;
        B[I]:=(Y[I+1]-Y[I])/S-(C[I]+R)*S;
    end;
write('S(x) for x = ');read(Z); writeln;
if (X[N]-X[O])=0 then Q:=0
            else Q:=(X[N]-X[O])/abs(X[N]-X[O]);
K:=-1;
repeat I:=K; K:=K+1; until (Q*Z<Q*X[K]) or (K=N) ;
Q:=Z-X[I]; T:=((D[I]*Q+C[I])*Q+B[I])*Q+Y[I]; writeln(T);
end.

program ROMBERG(input,output);
const EPS = 1.OE-7;
var    I                      : array[0..7] of real;
    Ia,S,Fl,A,B,H,X,Q     : real;
    K,J,N                 : integer;

function F(x:real) : real; begin F:= ln(x)/x; end;

begin
    write('Grenze A = '); read(A); writeln;
    write('Grenze B = '); read(B); writeln;
    H:=B-A; N:=1; X:=1; Fl:=F(X); X:=B; I[0]:=H*(Fl+F(X))/2;
    for K:=1 to 7 do
        begin
            S:=0; H:=H/2; N:=2*N; Q:=1; J:=1;
            while J<N do
                begin X:=A+J*H; S:=S+F(X); J:=J+2; end;
            I[K]:=I[K-1]/2+S*H;
            for J:=K-1 downto O do
                begin Q:=4*Q; I[J]:=I[J+1]+(I[J+1]-I[J])/(Q-1); end;
            writeln(I[O]); Ia:=abs(I[O]);
            if Ia<1 then Ia:=1;
            if abs(I[1]-I[O])<EPS*Ia then begin writeln(I[O]); halt; end;
        end;
    writeln(I[O]);
end.
```

---

510

Anhang: Pascal-Programme

```txt
program VollstElliptInt(input,output);
const pi = 3.14159265359;
    EPS = 1.0E-9;
var Al,Bl,E,K,A,B,C,D: real;

begin
    write('K= '); read(K); writeln;
    if K<1 then
        begin
            A:=1; B:=sqrt(1-K*K);
            C:=K; D:=2; E:=C*C;
            repeat
                begin
                    Al:=(A+B)/2; Bl:=sqrt(A*B); C:=(A-B)/2;
                    E:=E+D*C*C; A:=Al; B:=Bl;D:=2*D;
                end;
            until C<EPS;
            writeln('K(k)= ',pi/2/A);
            writeln('E(k)= ',pi/2/A*(1-E/2));
        end
    else writeln('fail');
end.

program GAUSS(input,output);
const maxdim = 50;
    EPS = 1.0E-09;
type Typ1 = array[0..maxdim,0..maxdim] of real;
    Typ2 = array[0..maxdim] of real;
    Typ3 = array[0..maxdim] of integer;
var L,K,I,J,N,M,S,V,U,P : integer;
        A : Typ1;
        B,C : Typ2;
        F : Typ3;
        Y,X,D : real;
        E : char;

procedure Scalar1(U,V,I:integer; A:Typ1; B:Typ2; X:real; var Y:real);
begin
    Y:=X; while U<=V do begin Y:=Y+A[I,U]*B[U]; U:=U+1; end;
end;

procedure Scalar2(K,U,V: integer; A: Typ1; X: real; var Y: real);
begin
    Y:=X; while K>0 do begin K:=K-1; Y:=Y+A[U,K]*A[K,V]; end;
end;

begin
    write('DIMENSION N = '); read(N); writeln;
    M:=N-1;
    writeln('A ZEILENWEISE');
    for I:=1 to N do
        begin
            for J:=1 to N do
                begin write('A',I:2,J:2,' = '); read(A[I-1,J-1]); end;
```

---

Anhang: Pascal-Programme

511

```pascal
writeln;
    end;
for I:=0 to M do
    begin
        Y:=0;
        for S:=0 to M do Y:=A[I,S]*A[I,S]+Y;
        if Y=0 then writeln('A singulaer') else C[I]:=1/sqrt(Y);
    end;
D:=1;
for K:=0 to M do
    begin
        L:=K; X:=0;
        for I:=K to M do
            begin
                Scalar2(K,I,K,A,-A[I,K],Y);
                A[I,K]:=-Y; Y:=abs(Y*C[I]);
                if Y>X then begin X:=Y; L:=I; end;
            end;
        if L<>K then
            begin
                D:=-D;
                for J:=0 to M do
                    begin Y:=A[K,J]; A[K,J]:=A[L,J]; A[L,J]:=Y; end;
                    F[L]:=F[K];
                end;
        F[K]:=L; D:=D*A[K,K];
        if X<EPS then exit;
        if K<M then for J:=K+1 to M do
            begin Scalar2(K,K,J,A,-A[K,J],Y); A[K,J]:=-Y/A[K,K]; end;
        end;
if abs(D)<EPS then begin writeln('A singulaer'); halt; end;
writeln('D=',D);
repeat
    writeln('RECHTE SEITE');
    for I:=1 to N do
        begin write('B',I:2,' = '); read(B[I-1]); writeln; end;
    for I:=0 to M do
        begin
            P:=F[I];
            if I<>P then begin X:=B[I]; B[I]:=B[P]; B[P]:=X; end;
        end;
    for I:=0 to M do
        begin Scalar1(0,I-1,I,A,B,B[I],Y); B[I]:=-Y/A[I,I]; end;
    for I:=M downto O do
        begin Scalar1(I+1,M,I,A,B,B[I],Y); B[I]:=-Y; end;
    writeln('ERGEBNIS:');
    for I:=1 to N do writeln('X',I:2,'=',B[I-1]);
    writeln('Neue rechte Seite (j/n) '');read(E);
until E='n';
end.
```

```txt
program LEVERRIER(input, output);
const   max = 50;
type   Typl = array[0..max, 0..max] of real;
```

---

512

Anhang: Pascal-Programme

```csv
var    I,J,K,L,N  : integer;
        A,B           : Typ1;
        X,S           : real;

procedure Shift;
var   I  : integer;
begin
    S:=0;
    for I:=1 to N do  S:=S+B[I,I];
    S:=S/K; writeln('C',K:2,' = ',-S); K:=K+1;
    for I:=1 to N do  B[I,I]:=B[I,I]-S;
end;

begin
    write('DIMENSION N = '); read(N); writeln;
    writeln('A ZEILENWEISE');
    for I:=1 to N do
        begin
            for J:=1 to N do
                begin
                    write('A',I:2,J:2,' = '); read(A[I,J]); B[I,J]:=A[I,J];
                end;
        end;
    writeln('C',O:2,' = ',l:2); K:=1;
    while K<=N-2 do
        begin
            Shift;
            for J:=1 to N do
                begin
                    for I:=1 to N do B[I,O]:=B[I,J];
                    for I:=1 to N do
                        begin
                            X:=0;
                            for L:=1 to N do X:=X+A[I,L]*B[L,0];
                            B[I,J]:=X;
                        end;
                    end;
            end;
        Shift; S:=0;
        for L:=1 to N do S:=S+A[1,L]*B[L,l];
        writeln ('C',K:2,' = ',-S);
end.

program Jacobi(input,output);
const maxgrad = 50;
type  Typ1     = array[l..maxgrad,l..maxgrad] of real;
var    K,W,U,N,M,I,J,P,Q,V,X      : integer;
        A,B                      : Typ1;
        S,R,F,G,E,C,D          : real;

procedure Rot(C,D: real; U,V,W,X: integer; var A: Typ1);
var    F,G: real;
begin G:=A[U,V]; F:=A[W,X]; A[W,X]:=C*F-D*G; A[U,V]:=D*F+C*G; end;
```

---

Anhang: Pascal-Programme

513

```pascal
begin
    write('DIMENSION N = '); read(N); M:=N-1;
    for I:=0 to M do
        begin
            for J:=I to M do
                begin
                    if I=J then B[I,I]:=1
                    else begin B[I,J]:=0; B[J,I]:=0; end;
                    write('A',I+1:2,J+1:2,' = '); read(A[I,J]);
                end;
            end;
        repeat
        S:=0;
        for P:=0 to M-1 do
            begin
                for Q:=P+1 to M do
                    begin
                        R:=A[P,Q]; F:=A[P,P]; G:=A[Q,Q]; A[P,Q]:=0;
                        if (abs(R)+abs(F)<=abs(F)) and
                            (abs(R)+abs(G)<=abs(G)) then R:=0
                        else
                            begin
                                E:=(G-F)/2/R;
                                if E=0 then E:=1
                                else
                                    if E>0 then E:=l/(E+sqrt(1+E*E))
                                    else          E:=l/(E-sqrt(1+E*E));
                                C:=l/sqrt(1+E*E); D:=C*E;
                                A[P,P]:=F-E*R; A[Q,Q]:=G+E*R;
                                if P>0 then
                                    for I:=0 to P-1 do Rot(C,D,I,Q,I,P,A);
                                if Q<>P+1 then
                                    for K:=P+1 to Q-1 do Rot(C,D,K,Q,P,K,A);
                                if Q<>M then
                                    for J:=Q+1 to M do Rot(C,D,Q,J,P,J,A);
                                for J:=0 to M do Rot(C,D,Q,J,P,J,B);
                            end;
                            S:=S+abs(R);
                        end;
                    end;
until S=0;
for I:=0 to M do writeln('X',I+1:2,' = ',A[I,I]);
for I:=0 to M do
    begin
        writeln(I+1:2,'.Eigenvektor:');
        for J:=0 to M do writeln(B[I,J]);
    end;
end.
```

```txt
program BAIRSTOW(input,output);
label Start;
const maxgrad = 50;
EPS=1.OE-07;
```

---

514

Anhang: Pascal-Programme

```pascal
Steps=30;
var N,M,I,K : integer;
B,C : array[O..maxgrad] of real;
U,V,S,BK,BK1,BK2,CK,CK1,CK2,Det : real;

procedure Quadr_gleichg(var U,V: real);
var X,Y,W : real;
begin
X:=U/2; Y:=X*X+V; W:=sqrt(abs(Y));
if Y=0 then writeln('doppelte Wurzel:',X)
else
begin
write('2 Wurzeln:');
if Y>0 then
begin
if X>=0 then writeln(X+W,',',-V/(X+W))
else writeln(X-W,',',-V/(X-W));
end
else writeln(X,'+-i*',W);
end;
end;

begin
write('Polynomgrad = '); read(N); writeln;M:=N;
for I:=0 to N do
begin write('a',I:2,' = '); read(B[I]); writeln; end;
while M>2 do
Start: begin
write('Startwert UO = '); read(U); writeln;
write('Startwert VO = '); read(V); writeln;
S:=0;
repeat
BK:=0; BK1:=0; CK:=0; CK1:=0;
for K:=0 to M-1 do
begin
CK2:=CK1; CK1:=CK; BK2:=BK1; BK1:=BK;
BK:=B[K]+U*BK1+V*BK2;
C[K]:=BK;
CK:=BK+U*CK1+V*CK2;
end;
BK2:=BK1; BK1:=BK; BK:=B[M]+U*BK1+V*BK2; C[M]:=BK;
Det:=CK1*CK1-CK2*CK;
if Det=0 then
begin writeln('Neue Startwerte!’); goto Start; end;
U:=U+(BK*CK2-BK1*CK1)/Det; V:=V+(BK1*CK-BK*CK1)/Det;
S:=S+1;
if S=Steps then
begin writeln('Neue Startwerte!’); goto Start; end;
until abs(BK1)+abs(BK)<EPS;
Quadr_gleichg(U,V); M:=M-2;
for K:=0 to M do B[K]:=C[K];
end;
if M=1 then writeln('reelle Wurzel: ',-B[1]/B[0])
else begin U:=-B[1]/B[0]; V:=-B[2]/B[0]; Quadr_gleichg(U,V); end;
end.
```

---

Anhang: Pascal-Programme

515

```matlab
program NLSQ(input,output);
const M = 6;
    N = 3;
    P = 4;
type Typ1 = array[0..N] of real;
    Typ2 = array[0..M] of real;
    Typ3 = array[0..M,0..P] of real;
var X : Typ1;
    F,T,Y : Typ2;
    A : Typ3;
    I,L,J : integer;
    Lambda,FO,FK,D,B,C,Dl,Bl,Cl : real;
```

```txt
function Fn(D,B,C: real;T: Typ2;Y: Typ2;var F: Typ2): real;
var I : integer;
    Q : real;
begin
    Q:=0;
    for I:=1 to M do
        begin F[I]:=Y[I]-D-B*exp(C*T[I]); Q:=Q+F[I]*F[I]; end;
    Fn:=sqrt(Q);
end;

procedure Linfit(var X: Typ1; var A: Typ3);
var I,J,K          : integer;
    S,F,V          : real;
begin
    for I:=1 to N do
    begin
        S:=0;
        for J:=I to M do S:=S+A[J,I]*A[J,I];
        if S=0 then
            begin writeln('Matrix singulaer'); halt; end;
        V:=sqrt(S);
        if A[I,I]>0 then V:=-V;
        X[I]:=V; F:=S-V*A[I,I]; A[I,I]:=A[I,I]-V;
        for K:=I+1 to N+1 do
            begin
                S:=0;
                for J:=I to M do S:=S+A[J,I]*A[J,K];
                S:=S/F;
                for J:=I to M do A[J,K]:=A[J,K]-A[J,I]*S;
            end;
    end;
    X[N]:=A[N,N+1]/X[N];
    for I:=N-1 downto 1 do
        begin
            S:=A[I,N+1];
            for J:=I+1 to N do S:=S-A[I,J]*X[J];
            X[I]:=S/X[I];
        end;
end;
```

---

516

Anhang: Pascal-Programme

```pascal
begin
    for I:=l to M do
        begin write('t(i)= '); read(T[I]); write('y(i)= '); read(Y[I]);
        end;
    write('a,b,c ='); read(D,B,C);
    FK:=Fn(D,B,C,T,Y,F); FO:=FK; L:=0;
    repeat
        for I:=l to M do
            begin
                A[I,1]:=l; A[I,2]:=exp(C*T[I]);
                A[I,3]:=B*T[I]*exp(C*T[I]); A[I,4]:=F[I];
            end;
        Linfit(X,A); Lambda:=l;
        repeat
            Dl:=D+Lambda*X[1]; Bl:=B+Lambda*X[2];
            Cl:=C+Lambda*X[3]; FK:=Fn(Dl,Bl,Cl ,T,Y,F);
            if FK<FO then exit;
            Lambda:=Lambda/2;
        until Lambda<0.002;
        if Lambda<0.002 then exit;
        if FK<FO then begin D:=Dl; B:=Bl; C:=Cl; FO:=FK; end;
        L:=L+1;
    until L=30;
    writeln('Steps,a,b,c =',L,D,B,C);
end.
```
