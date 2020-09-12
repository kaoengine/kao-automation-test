Hoạt động testing được coi là một phần trong quy trình phát triển phần mềm dù ở bất cứ mô hình nào. Chỉ khác ở chỗ nó nên được thực hiện lúc nào và làm ra làm sao ?

Cá nhân tôi chứng kiến và trải qua một số công ty và cho tới bây giờ cũng nhận ra nhiều mặt hạn chế. Xin được chia sẻ từ góc nhìn của tôi.

1. Vấn đề nội tại trong nhóm QA.
Với cách làm truyền thống thì testing được coi như là chốt chặn cuối cùng trước khi release. Điều này ko sai nhưng nó vô tình làm cản trở và làm chậm quá trình release. Thông thường khi release một phiên bản mới từ lúc tìm hiểu yêu cầu cho tới khi hoàn thành. DEv mất x ngày và Test mất y ngày nhưng nếu Dev tốn thêm z ngày mà vẫn muốn đảm bảo tiến độ thì đồng nghĩa việc test chỉ còn y-z ngày.

Đó là lý do vì sao đôi khi tester phải OT. Ngay cả khi chuẩn chỉ ai làm đúng thời gian của người đó thì trong hoạt động test vẫn còn lộ ra nhiều bước tốn thời gian, trong đó có việc update kết quả test cases. Nó hoàn toàn làm bằng tay. Các bạn Tester phải nhập từng chữ passed lên công cụ quản lý như excel, testrail, testlink.... hoặc các công cụ quản lý test khác, mà chỉ để phục vụ cho công tác báo cáo. Cá nhân tôi nghĩ những cases passed ko làm hại ai. Nên dù quản lý hay dev có biết hay ko biết nó cũng chẳng ảnh hưởng gì. Chúng ta chỉ cần tạo báo cáo liệt kê các cases KHÔNG PASS trong test plan là đủ.

Một số công ty tổ chức nhân sự chồng chéo. Họ tách Tester thành một department riêng và manager của bộ phận này sẽ làm nhiều vụ điều tiết người cho các dự án, thu thập báo cáo công việc các thành viên. Điều này có vẻ như tốt nhưng nếu họ không chọn việc show các kết quả test dựa trên các chỉ số xanh, đỏ ( pass, fail) để báo cáo thì có lẽ tester ko tốn thời gian để thực hiện các công việc không mất ý nghĩa như đã nêu trên. Những điều họ thường làm chỉ để lý giải cho việc họ đang cố gắng đạt KPI nào đó hoặc làm màu thành tích với các thông số. Về mặt ý nghĩa là ko cần thiết chỉ để "diễn" về mặt thành tích cá nhân hay phòng ban.

Bạn biết đấy Tester thường có sự kiên nhẫn vì công việc nó đòi hỏi sự tỷ mẫn, chi tiết. Do đó dễ nhận thấy nữ chiếm đa số vì một trong tính cách của nữ là sự kiên nhẫn. Nhưng họ chỉ có y ngày trong một chu kỳ phát triển phần mềm và liệu những gì chi tiết, tỷ mẫn mà lại làm nhanh. Liệu có phải là xung đột. Mà không làm nhanh thì lại làm chậm quá trình release.

2. Vấn đề chung trong toàn bộ dự án
Hoặc động testing luôn thực hiện sau khi Dev đã hoàn thành xong công việc của mình: Đây là cách làm nó mang ý nghĩa làm an lòng người quản lý dự án hoặc các ông chủ.

Về cơ bản testing là một trong những hoạt động để phát triển phần mềm nhưng với các làm này khi mà gạo đã vào nồi và lên lửa thì chưa biết nó thành cơm hay cháo. Có nghĩa là sau khi đã thành hình họ mới test thì nó chỉ mang ý nghĩa checking chứ không còn test nữa. Nên gọi họ là checker thì đúng hơn là tester. Việc của họ là báo lại cho bạn biết kết quả nồi cơm đó đã chín chưa để mang cho người dùng ăn. Nếu nó thành cháo thì báo lại nó là cháo hoặc thậm trí tệ hơn nó bị khê cháy và khét. Vậy sau khi nhận được kết qủa này ta làm gì? Đi mà rửa nồi mà nấu lại nồi khác thôi nhưng gạo ở đâu ra mà nấu lại. Tốn chi phí cho ông chủ.

Hãy coi phần mềm là nồi cơm đó. Khi mà test chỉ thực hiện công việc của mình sau khi dev làm xong. Họ phát hiện ra bug sẽ lại tốn thời gian đưa phần mềm trở lại cho dev để việc bảo trì, sửa chữa, fix bug hoặc làm mới cái thiếu. Lại gây chậm trễ.

Tóm lại quy trình có nhiều cái hạn chế. Bản thân việc thực hiện test cũng còn nhiều sự hạn chế mất thời gian.

Nhiều nơi đã áp dụng Agile để mọi thứ nhanh hơn nhưng lại biến nó thành mô hình thác nước thu nhỏ. Chỉ là họ chắt nước từ bình lớn sang các bình nhỏ hơn còn nước trong bình vẫn mùi vị ấy

Vậy làm sao để giải quyết vấn đề này

Không cần quan tâm các chúng ta vận hành quản lý như thế nào. Nhưng tập trung cho sự phản hồi sớm hơn là báo cáo.
Thay vì hoạt động độc lập như một internal service, thực hiện Test sau khi hoàn thành thì hãy test nó trước khi làm.
Làm sao để thực hiện nó. Làm sao để có phản hồi nhanh nhất, làm sao để tất cả đều chung trên một chiếc thuyền. Từ khoá là tự động hoá ( Automation Test)

Sau một thời gian hệ thống tích hợp nhiều chức năng vào hơn đồng nghĩa với số lượng những thứ cần test nhiều hơn. Họ không còn đủ thời gian làm test và giải pháp lúc này là tìm cái gì đó có thể tự động hóa một phần công việc của họ (QA).

Câu hỏi lúc này là vậy chúng ta sẽ tự động hóa phần công việc nào ? Ai là người đưa ra các quyết định sẽ tự động hóa cái nào và không tự động hóa cái nào.

1. Automate the wrong things
Tự động hóa là mục tiêu xứng đáng để làm. Nhưng trước khi làm công việc gì đó việc cân nhắc lợi ích đạt được có đáng để bỏ công sức, đáng để làm.

Điều gì xảy ra nếu bạn không hề tham gia vào quá trình xây dựng nó và chỉ kiểm tra nó sau khi nó đã hoàn thành.

Tôi kể cho bạn nghe một ví dụ có thật trong nhà tôi: Tôi cần lắp cái điều hòa và một trong công việc phải làm là thay lại bộ cửa sổ để cho khí lạnh không lọt ra ngoài. Cánh cửa hiện tại được thiết kế theo kiểu của những năm 198x. Nó có những cái khe song song theo chiều từ trên xuống, khó có thể lấp kín toàn bộ số khe này, nếu có nó cũng rất mất mỹ quan. Và tôi quyết định thay cửa khung nhôm. Tôi ở xa ko có ở nhà để xem họ làm. Sau khi xong người nhà báo giá thanh toán và kết thúc mong muốn của tôi. Rồi một ngày tôi trở về thấy cánh cửa được lắp bên trong phòng. Mở ra hay đóng vào là ở phía bên trong. Về cơ bản mục đích của tôi đã được hoàn thành vì cửa có thể mở ra và đóng vào và kín. (done) nhưng sau khi quan sát tôi tự hỏi điều gì xảy ra nếu vào mùa mưa. Cái cánh cửa trở thành một tấm chắn giúp nước mưa sẽ chảy toàn bộ vào trong phòng, còn toàn bộ ô cửa đóng vài trò như cái miệng cốc hứng nước mưa nếu mưa kèm gió nó tạt vào.

Để sửa chữa điều này có lẽ tôi phải bỏ thêm tiền để lắp viền cao su hoặc đại loại các gì đó nhằm chống nước chảy ngược vào trong. hoặc phải gỡ nó ra rồi lắp ra bên ngoài ( tốn chi phí). Tôi sẽ ko phải trả nó nếu như tôi đứng đó và nói lên ý kiến của mình trước khi họ làm.

Phần mềm cũng không khác. Bạn ko tham gia quá trình tìm hiểu và phát triển bạn sẽ giống bác tôi ở nhà. thấy họ làm xong vào đẩy cánh cửa thấy nó có thể mở ra, đóng vào và cảm thấy nó làm cho căn phòng kín hơn là ok. thanh toán tiền rồi.

Đấy là những thứ có thể wrong things. Tồi tệ hơn là bạn có thể tự động hóa cả bug của dev ( đương nhiên không phải bug liên quan UI, tới validation hay thứ mà dễ dàng nhận ra ma là bug liên quan tới nghiệp vụ)

2. Missing key scenarios
Tạm coi phần 1 là lỗi của Dev khi họ tạo ra những thứ wrong thing và mình test theo những thứ wrong things đó.

Còn trong phần này là sai làm từ phía QA. Nguyên nhân dẫn tới sai lầm này xuất phát từ nhiều nguyên nhân. Trong đó cách làm truyền thống (như đã đề cập ở trên là không tham gia vào quá trình phát triển) chỉ có thể giúp họ hiểu một cách hời hợt.

Đối với lớp quản lý thượng tầng mà nói họ sẽ cảm thấy yên tâm hơn nếu số lượng test cases nhiều. Càng nhiều càng tốt. Nó khiến họ nghĩ rằng mọi cái sẽ không thể bị bỏ sót. Họ viết quá nhiều test cases chỉ để check UI và Validation. Họ lý giải rằng, bug nào thì cũng là bug.

Bạn hãy nghĩ đến cái bánh gato sinh nhật đi. Mọi thứ lung linh bên ngoài chỉ là đồ trang trí và không mấy khi ai ăn đồ trang trí cả. ông cha ta cũng có câu tốt gỗ hơn tốt nước sơn. Chất lượng của một cái ghế gỗ phụ thuộc vào chất liệu gỗ chứ ko phải cái lớp sơn bên ngoài.

Số lượng automated tests không phải là vấn đề nếu như một kịch bản không chỉ rõ ràng ra được nó đang check cái gì và giá trị mà issue nó có thể detect ra. Nhiều không nói lên được điều gì nó chỉ nói lên rằng những thứ đó không có giá trị. Nhìn vào thực tế cái gì nhiều thường thì là do dễ làm mà cái gì dễ làm liệu có phải là thứ quý giá ?

Vậy làm sao để xác định được đâu là key scenarios, đâu là cái quý giá ?

Chúng ta cần có một hội đồng thẩm định. Tại sao chúng ta không tổ chức một buổi "scenarios workshop" mỗi tuần hay mỗi tháng. Nơi chúng ta cùng nhau bàn bạc về nói. Một cái đầu của dev làm sao hơn nếu có thêm môt cái đầu của QA và các bên khác. ( collaboration)

Nhiều QA luôn tỏ ra mặc cảm tự ti cho rằng Dev luôn trên họ một bậc nên không dám ngồi chung bàn..... điều này có đúng ? Nó sẽ có trong phần 3: "QA vs Dev ai thông minh hơn ai trong phát triển phần mềm"