Hi there! 

New macbooks is great, but are they great with docker? 

I wraped a geekbench inside a docker container and tested it. And some community members added their results as well. 

Main idea — for mac, put half of your CPU to docker, then run 

```
docker run --rm -ti ctrlok/geekbench:x86
 
# or 

docker run --rm -ti ctrlok/geekbench:m1 # for m1 or arm
```

Linux and windows machines had a lower overhead in docker mostly because of native implementation. Still, yay for them. 
Also, x86 docker qemu emulation on M1 pretty aweful, but nice to have it. 

Want to add something? Feel free to create a PR

# Multycore

| Name                                                                      | Native              | Docker x86 | Docker aarch64 |
| ------------------------------------------------------------------------- | ------------------- | ---------- | -------------- |
| MacBook Pro 16'' (10cpu 2021)                                             | 12533               | 500        | 7336           |
| MacBook Air M1                                                            | 7541                |            | 5411           |
| Hakintosh i9 10900K                                                       | 11232               | 5099       |                |
| MacBook Pro 13'' 2020, 2 GHz Quad-Core Intel Core i5                      | 4156                | 3233       |                |
| MacBook Pro (16-inch Late 2019) Intel Core i9-9880H                       | 6116                | 3299       |                |
| macbook pro 15 2018 (i7-8750H                                             |                     | 4594       |                |
| AMD Ryzen 9 5950X, windows                                                | 16176               | 16468      |                |
| Dell Latitude 5400      | 4123                | 4123       |                |
| MacBook Pro (13-inch, 2020), 2,3 GHz Quad-Core Intel Core i7              | 4615                | 3988       |                |
| Lenovo Linux-5.14.10-1-MANJARO **на**AMD Ryzen 7 5800H 3200 MHz           | 7064                | 7064       |                |
| Desktop Linux-5.14.10-1-MANJARO **на**AMD Ryzen 7 2700 3200 MHz (8 cores) | 5975                | 5888       |                |
| MBP16 Intel i9-9880H                                                      | 6234                | 6044       |                |
| **Ноут** HP Ubuntu 21.10 **на** AMD Ryzen 5 4600H 3.00 GHz                | 4980 (windows 4895) | 4690       |                |
| Windows AMD Ryzen 7 5800HS                                                | 4280                |            |                |


# Singlecore

| Name                                                                      | Native             | Docker x86 | Docker aarch64 |
| ------------------------------------------------------------------------- | ------------------ | ---------- | -------------- |
| MacBook Pro 16'' (10cpu 2021)                                             | 1764               | 106        | 1660           |
| MacBook Air M1                                                            | 1721               |            | 1656           |
| Hakintosh i9 10900K                                                       | 1283               | 1353       |                |
| MacBook Pro 13'' 2020, 2 GHz Quad-Core Intel Core i5                      | 1042               | 865        |                |
| MacBook Pro (16-inch Late 2019) Intel Core i9-9880H                       | 976                | 1105       |                |
| macbook pro 15 2018 (i7-8750H                                             |                    | 954        |                |
| AMD Ryzen 9 5950X, windows                                                | 1604               | 1710       |                |
| Dell Latitude 5400 | 1109               | 1109       |                |
| MacBook Pro (13-inch, 2020), 2,3 GHz Quad-Core Intel Core i7              | 1300               | 1123       |                |
| Lenovo Linux-5.14.10-1-MANJARO **на**AMD Ryzen 7 5800H 3200 MHz           | 1387               | 1300       |                |
| Desktop Linux-5.14.10-1-MANJARO **на**AMD Ryzen 7 2700 3200 MHz (8 cores) | 1091 (windows 897) | 1085       |                |
| MBP16 Intel i9-9880H                                                      | 1053               | 1151       |                |
| **Ноут** HP Ubuntu 21.10 **на** AMD Ryzen 5 4600H 3.00 GHz                | 897 (windows 865)  | 810        |                |
| Windows AMD Ryzen 7 5800HS                                                | 1177               |            |                |
