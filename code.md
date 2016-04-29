---
layout: page
title: Code
permalink: /code/
---
## How to use the code?
### Encoding
1. Import an image
2. Write the message you want to encode in the variable Message in rgbtransform.m
3. run rgbtransform.m

### Decoding
1. Import the encoded image
2. run rgbitransform.m



### rgbtransform.m
1. Type in the message we want to hide and import image
2. Divides the 3D Image Matrice into 3 2D Matrices, where each matrice correspond to the R,G,B of the Image
3. Divides the message into 3 parts
4. Run the dctransform code to hide messages in each images
5. Combine the 3 images to form one RGB Image and saves the file

```python

Message = 'Type in the message here:';
Image = catc;

Ir = Image(:,:,1);
Ig = Image(:,:,2);
Ib = Image(:,:,3);

Mlen = length(Message);
Messager = Message(1:round(Mlen/3));
Messageg = Message(round(Mlen/3)+1:round(2*Mlen/3));
Messageb = Message(round(2*Mlen/3)+1:Mlen);

tIr = dctransform(Ir, Messager)/255;
tIg = dctransform(Ig, Messageg)/255;
tIb = dctransform(Ib, Messageb)/255;

finalimg = cat(3,tIr,tIg,tIb);

subplot(2,2,1); imshow(cat(3,Ir,Ig,Ib))
subplot(2,2,2); imshow(finalimg)

% imwrite(finalimg, 'C:\Users\jkim2\Documents\SigSys\Final Project\fftimage.jpg')
```



### dctransform.m
1. Discrete Cosine Transform (DCT)
2. Fast Fourier Transform Shift (FFTshift)
3. Hide message length in the middle
4. Encode message in the hiding region
5. Inverse FFTshift
6. Inverse DCT
7. Return ecoded image

```python
function t_img = dctransform(image_in, message)

% % %DCT transform, shift
D = dct2(double(image_in)); %DCT of image
Ds = fftshift(D); %make center low freq

% % %plot
% subplot(2,2,1);image(image_in);
% subplot(2,2,3);imshow(log(abs(Ds)),[]);

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
% subplot(2,2,4);imshow(log(abs(Ds)),[]);
end
```



### rgbitransform.m
1. Import encoded message
2. Divides the 3D image matrice into 3 2D matrices, where each matrice correspond to the R,G,B of the image
3. Run the idctransform code to decode messages in each images
5. Combine the 3 decoded messages to get the message

```python
Irgbt = finalimg; %transformed image

Irt = Irgbt(:,:,1)*255;
Igt = Irgbt(:,:,2)*255;
Ibt = Irgbt(:,:,3)*255;

idctransform(Irt)
idctransform(Igt)
idctransform(Ibt)
```



### icdtransform.m
1. DCT
2. FFTshift
3. Get the length of the message encoded in the middle
4. Print the message decoded from the hiding region

```python
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
music = [];
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
end
end
```
