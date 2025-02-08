function c = celldestiny (A,i,j,n)

if n < 2 && A(i,j) == 1 %när en levande cellen har mindre än 2 grannar, dör den
    c=0;
elseif (n==2 || n==3) && A(i,j) == 1 % När en levande cell har antigen 2 eller 3 grannar förblir den levande
    c=1;
elseif n > 3 && A(i,j) == 1 % när en levande cell har mer än 3 grannar dör den
    c= 0;
elseif A(i,j) == 0 && n==3 % när en död cell har 3 grannar kommer den till liv
    c=1;
else
    c=0; %om inget av villkoren uppfylls är cellen död
    
end 
end

