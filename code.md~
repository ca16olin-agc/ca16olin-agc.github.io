---
layout: page
title: Code
permalink: /code/
---

rgbtransform.m
```matlab
Message = 'Type in the Message here: hello TJ. Jong is here!';
Image = im2double(catc);

Ir = catc(:,:,1);
Ig = catc(:,:,2);
Ib = catc(:,:,3);

Mlen = length(Message);
Messager = Message(1:round(Mlen/3));
Messageg = Message(round(Mlen/3)+1:round(2*Mlen/3));
Messageb = Message(round(2*Mlen/3)+1:Mlen);

tIr = dctransform(Ir, Messager);
tIg = dctransform(Ig, Messageg);
tIb = dctransform(Ib, Messageb);

finalimg = cat(3,tIr/255,tIg/255,tIb/255);

subplot(2,2,1); image(cat(3,Ir,Ig,Ib))
subplot(2,2,2); image(finalimg)

imwrite(finalimg, 'C:\Users\jkim2\Documents\SigSys\Final Project\fftimage.jpg')
```



dctransform.m
```matlab
function t_img = dctransform(image_in, message)

% % %DCT transform, shift
D = dct2(double(image_in)); %DCT of image
Ds = fftshift(D); %make center low freq

% % %plot
% subplot(2,2,1);image(image_in);
% subplot(2,2,2);imagesc(log(abs(Ds)));

[M N] = size(D); 
ci = round(M/2)+1; 
cj = round(N/2)+1;

% % %Hiding Region
lr = round(M/5); 
hr = round(M/3);

% % %Message
mlen = length(message);

% % % Hiding the Message
m=1; 
r=0;

for (i=1:hr)
    for (j=1:hr)
        r = sqrt(i*i + j*j);
        if ((r > lr) && (r < hr))
            if (m <= mlen)
                Ds(i+ci, j+cj) = double(message(m));
                Ds(i+ci, -j+cj) = Ds(i+ci, j+cj); % copy over to each quadrant
                Ds(-i+ci, j+cj) = Ds(i+ci, j+cj);
                Ds(-i+ci, -j+cj) = Ds(i+ci, j+cj);
                m = m+1; 
            end; 
        end; 
    end; 
end;
Ds(1,1) = mlen;

t_img = idct2(ifftshift(Ds));

% % %plot tranformed
% subplot(2,2,3);image(t_img);
% subplot(2,2,4);imagesc(log(abs(Ds)));
end
```



rgbitransform.m
```matlab
Irgbt = finalimg; %transformed image

Irt = Irgbt(:,:,1)*255;
Igt = Irgbt(:,:,2)*255;
Ibt = Irgbt(:,:,3)*255;

idctransform(Irt)
idctransform(Igt)
idctransform(Ibt)
```



icdtransform.m
```matlab
function idctransform(It)

D2 = dct2(It); 
Ds2 = fftshift(D2); 

mlen2 = uint8(Ds2(1,1));

[M2 N2] = size(D2); 
ci2 = round(M2/2)+1; 
cj2 = round(N2/2)+1;

% % %Hiding Region
lr2 = round(M2/5); 
hr2 = round(M2/3);

m2 = 1;
r2 = 0;
for (i=1:hr2)
    for (j=1:hr2)
        r2 = sqrt(i*i + j*j);
        if ((r2 > lr2) && (r2 < hr2))
            if (m2 <= mlen2)
                fprintf(1, '%c', char(uint8(Ds2(i+ci2, j+cj2))))
                m2 = m2 +1; 
            end; 
        end; 
    end; 
end;

end
```
