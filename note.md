***scroll-padding-top: dùng để tạo padding của scroll span hay làm dùng id để tới phần tử, nó sẽ để bên trên 1 khoảng padding

***sử lí css cho thanh scroll bar
::-weklit-scrollbar: thanh cuộn(the scrollbar)
::-webkit-scrollbar-track: thanh tiến trình(phần process bar): phần hiển thị của thanh cuộn lên màn hình
::-webkit-scrollbar-thumb: thanh cuộn nhỏ nhỏ cầm để kéo
::-webkit-scrollbar-conner: nơi giao nhau giữa hai thanh cuộn, ở góc

***padding-top: 50%, 100%: nghia la chieu cao = 50, 100% chieu rong
***padding-right, left: x%, tuc la padding theo chieu rong cua cha no x%

***grid-template-column: repeat(auto-fit, minmax($val, 1fr))
***grid-template-column: repeat(auto-fill, minmax($val, 1fr))

có nghĩa là, auto-fit thì luôn set cho các phần tử con bên trong lấp đầy 1 hàng, cho dù kích thước nào đi nữa
             auto-fill thì set cho đủ số lượng, không nhất thiết là lấp đầy khoảng trống
minmax: giá trị nhỏ nhất là $val, max 1 fr cho all phần tử giống nhau, nếu mà quá nhiều con mà all chia đều width nhỏ hơn min $val,
thì nó sẽ tự động xuống hàng


***css clip-path maker : tra google để làm clip-path và được nó generate cho

*** cái div sổ xuống có thể dùng clip-path thay vì height
*** trong font-awesome, các class set icon có thể ghi đè lên nhau, do đó không cần set class cũ khi làm class mới

*muốn set cho font nhỏ hơn khi responsive, các chữ cái, padding đều làm theo rem hết, rồi sau đó thay đổi html font-size thành 55%, 50% ......

*flex-grow: set cho phan tu gap may lan cac phan tu con lai trong 1 flex
----mac dinh cac phan tu co flex-grow = 0, ko co theo do rong cua cha
*flex-shirk: no se co lai theo do rong cua container
---mac dinh la 1 se co lai, neu set la 0 thi no se ko co lai va lay theo width cua chinh no
*flex-basis: set cho phan tu co chieu rong, hay chieu cao dua theo row hay columnn, no se de len thuoc tinh width va height cua phan tu

flex: one ===> flex-grow
flex: one two ===> flex-grow flex-shirk  or   flex-grow flex-basis
flex: one two three ===> grow, shirk, basis

mac dinh : grow0 shirk1 basis:auto

-----------------------------
    Khi độ rộng container giảm xuống so với ban đầu thì chúng ta tính theo flex-shrink và ngược lại khi độ rộng container tăng lên so với ban đầu thì tính theo flex-grow. Phần tăng lên hay giảm xuống của container sẽ chia tỉ lệ cho flex-shrink hay flex-grow tương ứng của các phần tử


    Khi các bạn resize trình duyệt lại sao cho container còn 430px thì lúc này chúng ta sẽ mất là 640 – 430 =  210px. Ô số 1 do có flex-shrink: 1 nên nó mất 70px(chiều rộng của nó bây giờ sẽ là 300 – 70 = 230px), còn ô số 2 có flex-shrink: 2 nên sẽ mất đi 140px(chiều rộng sẽ còn 300 – 140x = 160px).

    Các bạn lại resize trình duyệt tiếp cho đến khi độ rộng container xuống 340px thì chúng ta mất 640 – 340  = 300px. Ô số 1 có flex-shrink: 1 nên sẽ mất 100px(còn 200px) còn ô số 2 sẽ mất 200px(còn 100px) do có flex-shrink: 2.

    Tương tự với flex-grow. Khi tăng độ rộng container lên 940px. Thì container được tăng thêm 300px(640 + 300 = 940). Ô số 1 có flex-grow: 2 nên sẽ tăng lên thêm 200px(tổng sẽ là 500px) còn ô số 2 có flex-grow: 1 nên sẽ chiếm 1/3 là 100px nên nó sẽ tăng thêm độ rộng 100px(tổng sẽ là 400px).
-----------------------------


----NOTE: cách dùng flex để set width ko cần dựa vào set width % của các phần tử
sử dụng flex: 1 1 42rem, và dùng flex-wrap,,,,, màn hình sẽ co lại cho đến khi nào mà width phần tử < 42rem thì nó sẽ tự độnmg xuống dòng
do ta set flex-basis: 42rem set do rong, do cao theo row, col

---NOTE: dufng thuộc tính mới columns trong css: columns: min-width max-col
cho các phần tử con, có thể set gap cho cac cot, column-count: cố định