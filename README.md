# Request

> 用于在浏览器做多个接口的流程编排和数据聚合

## <svg t="1654867482960" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="6545" width="32" height="32"><path d="M512 1024c-106.514286 0-184.457143-6.742857-231.657143-20.114286-19.885714-5.6-34.971429-12.571429-46.057143-21.142857-16.571429-12.8-21.942857-27.314286-23.657143-37.257143l-0.114285-0.8-14.057143-104.457143-7.771429-0.457142-63.657143-461.371429 9.371429 0.342857-6.057143-45.257143H76.457143L100.342857 193.142857c2.857143-16.8 12.342857-30.971429 25.485714-40l13.714286-77.942857c5.028571-28.457143 29.828571-49.028571 59.085714-49.028571h437.6C645.6 10.285714 662.285714 0 681.371429 0h142.857142C851.428571 0 873.942857 21.028571 876.571429 48.914286l0.571428 6.4c3.542857 6.057143 6.057143 12.685714 7.314286 19.771428l13.714286 77.942857c13.142857 9.028571 22.628571 23.2 25.485714 40l23.885714 140.342858h-52l-6.057143 45.257142 9.371429-0.342857-63.657143 461.371429-7.771429 0.457143-14.057142 104.457143-0.114286 0.8c-1.6 9.942857-7.085714 24.457143-23.657143 37.257142-11.085714 8.571429-26.171429 15.542857-46.057143 21.142858C696.457143 1017.257143 618.514286 1024 512 1024z" fill="#25467A" p-id="6546"></path><path d="M512 231.314286H165.828571L260.571429 936.914286s6.057143 36.342857 251.428571 36.342857 251.428571-36.342857 251.428571-36.342857l94.742858-705.485715H512z" fill="#BBDEFB" p-id="6547"></path><path d="M512 435.771429c-165.371429 0-328.571429-5.028571-328.571429-5.028572l49.828572 361.028572c76.685714 4.571429 169.6 7.885714 278.742857 7.885714s202.057143-3.314286 278.742857-7.885714l49.828572-361.028572s-163.2 5.028571-328.571429 5.028572z" fill="#1E88E5" p-id="6548"></path><path d="M826.057143 54.057143c-0.114286-1.828571-1.142857-3.2-2.171429-3.2H681.142857c-1.028571 0-1.942857 1.371429-2.171428 3.2l-4.8 52.457143H830.857143l-4.8-52.457143z" fill="#EEEEEE" p-id="6549"></path><path d="M834.514286 84.228571c-0.8-4.228571-4.8-7.428571-9.485715-7.428571H198.971429c-4.685714 0-8.8 3.085714-9.485715 7.428571l-21.257143 120.8h687.542858L834.514286 84.228571z" fill="#F5F5F5" p-id="6550"></path><path d="M873.6 201.828571c-0.8-4.914286-4.914286-8.571429-9.6-8.571428H160c-4.685714 0-8.8 3.657143-9.6 8.571428l-13.942857 81.485715h751.085714l-13.942857-81.485715z" fill="#FFFFFF" p-id="6551"></path><path d="M512 720.8c-35.314286 0-64-28.685714-64-64 0-7.085714 5.714286-12.8 12.8-12.8s12.8 5.714286 12.8 12.8c0 21.257143 17.257143 38.4 38.4 38.4s38.4-17.142857 38.4-38.4c0-7.085714 5.714286-12.8 12.8-12.8s12.8 5.714286 12.8 12.8c0 35.428571-28.685714 64-64 64z" fill="#25467A" p-id="6552"></path><path d="M384 554.4m-38.4 0a38.4 38.4 0 1 0 76.8 0 38.4 38.4 0 1 0-76.8 0Z" fill="#25467A" p-id="6553"></path><path d="M640 554.4m-38.4 0a38.4 38.4 0 1 0 76.8 0 38.4 38.4 0 1 0-76.8 0Z" fill="#25467A" p-id="6554"></path><path d="M332.8 618.4h-51.2c-14.171429 0-25.6 11.428571-25.6 25.6s11.428571 25.6 25.6 25.6h51.2c14.171429 0 25.6-11.428571 25.6-25.6 0-14.057143-11.428571-25.485714-25.6-25.6zM742.4 618.4h-51.2c-14.171429 0-25.6 11.428571-25.6 25.6s11.428571 25.6 25.6 25.6h51.2c14.171429 0 25.6-11.428571 25.6-25.6 0-14.057143-11.428571-25.485714-25.6-25.6z" fill="#BBDEFB" p-id="6555"></path></svg> 功能

- [x] 支持并行的请求模式
- [x] 支持串行的请求编排
- [x] 能够灵活定义接口依赖
- [x] 不限制具体的请求库，可以用 XHR、Fetch、axios，只要请求函数能够满足 Promise 规范即可接入
- [x] 支持熔断机制
- [x] 支持重试机制，可以根据不同接口制定不同的重试次数
- [ ] 数据处理，支持多个请求数据的聚合、排序、分组等

## <svg t="1654867537281" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="6900" width="32" height="32"><path d="M454.4 851.885714c-81.257143 0-146.171429-13.942857-192.914286-41.257143-30.742857-18.057143-53.828571-42.628571-65.6-69.371428C120.914286 685.942857 66.285714 603.085714 33.485714 494.514286 4.342857 398.285714 0 304.685714 0 257.371429 0 190.057143 52.571429 130.285714 148 89.028571 230.628571 53.257143 339.428571 33.6 454.4 33.6c114.971429 0 223.771429 19.657143 306.4 55.428571 95.428571 41.257143 148 101.142857 148 168.342858v0.8c26.628571 7.885714 50.4 22.285714 69.485714 42.4 34.514286 36.342857 50.285714 86.857143 44.342857 142.057142-5.6 52-31.771429 101.714286-73.6 140.114286-36.914286 33.714286-84.457143 56.8-130.628571 63.085714-5.028571 0.685714-10.057143 1.257143-15.085714 1.6-25.828571 37.028571-56.114286 68.457143-90.514286 93.828572-11.771429 26.742857-34.857143 51.314286-65.6 69.371428-46.628571 27.314286-111.542857 41.257143-192.8 41.257143z" fill="#25467A" p-id="6901"></path><path d="M512 990.4c-130.4 0-253.6-22.285714-347.2-62.742857C58.514286 881.714286 0 815.657143 0 741.714286s58.514286-140 164.8-186.057143c93.485714-40.457143 216.8-62.742857 347.2-62.742857 130.4 0 253.6 22.285714 347.2 62.742857 106.285714 45.942857 164.8 112 164.8 186.057143s-58.514286 140-164.8 186.057143c-93.6 40.342857-216.8 62.628571-347.2 62.628571z" fill="#25467A" p-id="6902"></path><path d="M48 741.714286c0 110.857143 207.771429 200.8 464 200.8S976 852.685714 976 741.714286 768.228571 540.914286 512 540.914286 48 630.857143 48 741.714286z" fill="#FFFFFF" p-id="6903"></path><path d="M62.628571 729.942857c0 100.228571 201.142857 181.485714 449.371429 181.485714 248.114286 0 449.371429-81.257143 449.371429-181.485714S760.114286 548.457143 512 548.457143 62.628571 629.714286 62.628571 729.942857z" fill="#E0E0E0" p-id="6904"></path><path d="M186.4 714.285714C192 791.542857 339.428571 843.657143 515.657143 830.857143c176.228571-12.8 314.628571-85.828571 308.914286-163.085714-5.6-77.257143-153.028571-129.371429-329.371429-116.571429-176.114286 12.914286-314.514286 85.828571-308.8 163.085714z" fill="#BDBDBD" p-id="6905"></path><path d="M454.4 829.028571c-77.142857 0-138.171429-12.8-181.371429-38.171428-26.4-15.428571-46.285714-36.342857-56.228571-58.857143l-2.4-5.6-4.914286-3.657143C138.514286 670.628571 86.628571 591.542857 55.314286 487.885714 27.085714 394.514286 22.857143 303.428571 22.857143 257.371429c0-57.6 47.657143-109.942857 134.171428-147.428572C236.914286 75.428571 342.514286 56.457143 454.4 56.457143S672 75.428571 751.771429 109.942857c86.514286 37.485714 134.171429 89.828571 134.171428 147.428572v17.828571l16.342857 4.8c22.742857 6.742857 43.314286 19.2 59.428572 36.228571 29.828571 31.428571 43.428571 75.428571 38.171428 123.885715-5.028571 46.514286-28.571429 91.085714-66.4 125.714285-33.6 30.742857-76.685714 51.542857-118.285714 57.257143-4.571429 0.571429-9.028571 1.142857-13.485714 1.371429l-10.971429 0.685714-6.285714 9.028572c-24.342857 34.971429-53.028571 64.685714-85.257143 88.457142l-4.914286 3.657143-2.4 5.6c-9.942857 22.514286-29.828571 43.428571-56.228571 58.857143-43.085714 25.371429-104.114286 38.285714-181.257143 38.285714z" fill="#25467A" p-id="6906"></path><path d="M789.714286 599.885714c-37.257143 0-61.485714-14.057143-75.885715-27.085714-26.971429-24.342857-41.257143-62.742857-41.257142-111.2 0-39.428571 20.571429-78.742857 57.828571-110.742857 33.485714-28.685714 76-47.2 116.914286-50.971429 38.171429-3.542857 72.342857 8.457143 96.342857 33.714286 24.685714 26.057143 35.885714 62.857143 31.428571 103.885714-4.342857 40.342857-25.028571 79.428571-58.285714 109.828572-29.828571 27.314286-68 45.942857-104.685714 50.971428-8 1.028571-15.428571 1.6-22.4 1.6zM860.228571 361.142857c-2.514286 0-5.028571 0.114286-7.657142 0.342857-59.428571 5.485714-120 56-120 100.114286 0 29.6 7.314286 52.571429 20.685714 64.685714 11.314286 10.171429 28.342857 13.828571 50.742857 10.742857 48.914286-6.742857 105.371429-50.971429 111.314286-106.285714 2.4-22.171429-2.857143-41.257143-14.628572-53.714286-9.828571-10.514286-23.771429-15.885714-40.457143-15.885714z" fill="#C7C7C7" p-id="6907"></path><path d="M454.4 702.514286H235.2c0 26.971429 37.142857 101.257143 219.2 101.257143s219.2-74.285714 219.2-101.257143H454.4z" fill="#E0E0E0" p-id="6908"></path><path d="M454.4 257.371429H48C48 394.285714 85.257143 771.2 454.4 771.2S860.914286 394.285714 860.914286 257.371429H454.4z" fill="#EEEEEE" p-id="6909"></path><path d="M48 257.371429c0 118.514286 27.885714 417.142857 275.2 495.085714-156.571429-86.857143-222.742857-262.742857-214.285714-495.085714H48z" fill="#FFFFFF" p-id="6910"></path><path d="M860.914286 257.371429c0 118.514286-27.885714 417.142857-275.2 495.085714 156.571429-86.857143 222.742857-262.742857 214.285714-495.085714h60.914286z" fill="#E0E0E0" p-id="6911"></path><path d="M48 257.371429c0 97.142857 181.942857 175.885714 406.4 175.885714 224.457143 0 406.4-78.742857 406.4-175.885714S678.857143 81.6 454.4 81.6C229.942857 81.6 48 160.342857 48 257.371429z" fill="#FFFFFF" p-id="6912"></path><path d="M454.4 396.914286c-103.542857 0-200.571429-17.142857-273.257143-48.114286-61.828571-26.4-100.342857-61.485714-100.342857-91.428571s38.4-65.028571 100.342857-91.428572c72.685714-30.971429 169.714286-48.114286 273.257143-48.114286s200.571429 17.142857 273.257143 48.114286c61.828571 26.4 100.342857 61.485714 100.342857 91.428572s-38.4 65.028571-100.342857 91.428571c-72.571429 31.085714-169.714286 48.114286-273.257143 48.114286z" fill="#E0E0E0" p-id="6913"></path><path d="M454.4 189.257143c-251.542857 0-353.6 108.571429-351.2 110.857143 17.371429 17.371429 44.114286 34.4 77.942857 48.8 72.685714 30.971429 169.714286 48.114286 273.371429 48.114285s200.571429-17.142857 273.371428-48.114285c33.828571-14.4 60.571429-31.428571 77.942857-48.8 2.171429-2.4-99.885714-110.857143-351.428571-110.857143z" fill="#6D4C41" p-id="6914"></path><path d="M805.714286 300.114286c-4.914286 4.914286-10.628571 9.828571-17.028572 14.628571-24-24.571429-126.4-103.771429-334.285714-103.771428s-310.285714 79.2-334.285714 103.771428c-6.4-4.8-12.114286-9.714286-17.028572-14.628571-2.285714-2.285714 99.771429-110.857143 351.2-110.857143 251.657143 0 353.714286 108.457143 351.428572 110.857143z" fill="#FFCC80" p-id="6915"></path><path d="M454.4 674.514286c-35.314286 0-64-28.685714-64-64 0-7.085714 5.714286-12.8 12.8-12.8s12.8 5.714286 12.8 12.8c0 21.257143 17.142857 38.4 38.4 38.4s38.4-17.142857 38.4-38.4c0-7.085714 5.714286-12.8 12.8-12.8s12.8 5.714286 12.8 12.8c0 35.314286-28.571429 64-64 64zM288 508.114286c0 21.257143 17.142857 38.4 38.4 38.4s38.4-17.142857 38.4-38.4-17.142857-38.4-38.4-38.4c-21.142857 0-38.285714 17.142857-38.4 38.4zM544 508.114286c0 21.257143 17.142857 38.4 38.4 38.4s38.4-17.142857 38.4-38.4-17.142857-38.4-38.4-38.4-38.285714 17.142857-38.4 38.4z" fill="#25467A" p-id="6916"></path><path d="M275.2 572.114286H224c-14.171429 0-25.6 11.428571-25.6 25.6 0 14.171429 11.428571 25.6 25.6 25.6h51.2c14.171429 0 25.6-11.428571 25.6-25.6 0-14.171429-11.428571-25.6-25.6-25.6z m409.6 0h-51.2c-14.171429 0-25.6 11.428571-25.6 25.6 0 14.171429 11.428571 25.6 25.6 25.6h51.2c14.171429 0 25.6-11.428571 25.6-25.6 0-14.171429-11.428571-25.6-25.6-25.6z" fill="#FFCC80" p-id="6917"></path><path d="M215.771429 256.914286a47.771429 26.514286 0 1 0 95.542857 0 47.771429 26.514286 0 1 0-95.542857 0Z" fill="#FFCC80" p-id="6918"></path><path d="M276.685714 236.685714a47.771429 26.514286 0 1 0 95.542857 0 47.771429 26.514286 0 1 0-95.542857 0Z" fill="#FFCC80" p-id="6919"></path><path d="M733.977297 315.30235a34.742857 25.142857 22.626 1 0 19.345629-46.415511 34.742857 25.142857 22.626 1 0-19.345629 46.415511Z" fill="#FFCC80" p-id="6920"></path><path d="M225.313203 254.513313a21.6 32.457143 84.154 1 0 64.576683-6.611845 21.6 32.457143 84.154 1 0-64.576683 6.611845Z" fill="#FFF3E0" p-id="6921"></path></svg> Repobeats
![Alt](https://repobeats.axiom.co/api/embed/3a281333d1b629dfec0ef4bbf2cc493453c66d73.svg "Repobeats analytics image")

