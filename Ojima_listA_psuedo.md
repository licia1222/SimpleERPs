# SimpleERPs
Test new wireless caps

Matlab/Cogent

clear all;
close all;

% 2000+(850+600)*5=9250 ms/trial, 9300*160= 1,480 s/exp, =24.66 min/exp. without instuction
% ...textread...
[stiID,list,condition,correct,frame1,frame2,frame3,frame4,frame5,target,framenum,event]=textread('ethan_stimuli.txt','%f%s%s%f%s%s%s%s%s%f%f%f','delimiter','\t');
a=unidrnd(4,1,120);

 for r = 1:119
        while(a(1,r)==a(1,r+1))
            a(1,r+1)=unidrnd(4);
        end
end
index=randperm(30);
a4=linspace(1,59,30);
a3=linspace(2,60,30);
a2=linspace(61,119,30);
a1=linspace(62,120,30);

 for i=1:30
     a14(i)=a4(index(i));
 end
  for i=1:30
     a13(i)=a3(index(i));
  end
 for i=1:30
     a12(i)=a2(index(i));
 end
 for i=1:30
     a11(i)=a1(index(i));
 end

 k=1;
 j=1;
 l=1;
 m=1;
 a14=[a14,a14];
 a13=[a13,a13];
 a12=[a12,a12];
 a11=[a11,a11];
 
 for ii=1:120
     if(a(ii)==1)
         a(ii)=a11(k);
         k=k+1;
     elseif(a(ii)==2)
             a(ii)=a12(j);
             j=j+1;
     elseif(a(ii)==3)
             a(ii)=a13(l);
             l=l+1;
     elseif(a(ii)==4)
             a(ii)=a14(m);
             m=m+1;
     end
 end
 listA=a';
