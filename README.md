# just-another-respository
inputMatrixI=cell2mat((New_dataopenbidx(2:end,:)));
inputMatrixT=cell2mat((New_datax(2:end,:)));

outputMatrix=zeros(size((New_datax(2:end,:)),1),size((New_datax),2));


for i = 1:size((New_datax),2)
   
    temp=zeros(500,1);
    temp = macd(inputMatrix(:,i));
    outputMatrix(:,i)=temp;
end

 col_header_3 =New_datax(1,:);
 Table_MACD = [col_header_3;num2cell(outputMatrix)];
