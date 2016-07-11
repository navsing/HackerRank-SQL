select n, 
case 
when (p is null) then 'Root' 
when (n in (select p from bst)) then 'Inner'
else 'Leaf' end from bst order by n;
