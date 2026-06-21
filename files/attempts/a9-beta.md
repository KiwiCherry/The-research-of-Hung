
(vietnamese)

**Authors:** Hung Dinh Phu Dang  

**Date:** 17-18, June 2026  


Thay vì : "Làm sao để tính ra N đáp án vô hướng của N biểu thức nhanh nhất?" ; Thì : "Tại sao phải cần đáp án vô hướng trong khi ta chỉ cần ý nghĩa về mối quan hệ và khả năng "Total Order" (LƯU Ý RẰNG TÔI ĐÃ CHÈN DẤU NGOẶC KÉP VÀO!) của chúng?"

và "Liệu hầu như tất cả những bài toán quan trọng hiện nay về bản chất không thực sự cần scalar hay không?" ;

"Một nền tảng & môi trường trong khuôn khổ chặt chẽ và logic, nơi mà tự động N biểu thức có mối quan hệ tương tự với N scalars, từ đó việc tính toán ra N scalars là vô nghĩa; Thiết kế chặt chẽ để các trade-off là hợp lý để không thành 'rác' lý thuyết" ;

"Có thể tưởng tượng rằng, một khuôn khổ toán học mới, nơi khi ta điền input là N biểu thức, không cần phải tính ra scalars" ;

"Chỉ cần lý thuyết này có thể so sánh **bất kỳ 2 biểu thức bất kỳ** với nhau (< ; > ; =) và biết được 'khoảng cách' giữa chúng tương tự như scalars, hoặc chỉ cần cùng 'ý nghĩa và có thể thay thế', và các trade-off là hợp lý để không thành 'rác' lý thuyết, đây có thể là thứ chúng ta đang tìm?'

"Thực tại vật lý không hề đọc những con số. Vũ trụ không có con số 5V hay 30 độ."
Bản chất của một cánh tay robot di chuyển là sự tương tác giữa các biểu thức vật lý. Biểu thức dòng điện (một trường điện từ) tương tác với biểu thức cơ năng (cuộn dây và nam châm). Nó là sự khớp nối các trường năng lượng, không có bất kỳ một con số vô hướng nào thực sự tồn tại ở đó cả. Con số vô hướng (scalar) chỉ là thứ con người đẻ ra để đọc và hiểu thực tại, chứ thực tại không cần con số để vận hành. Nếu máy tính nối thẳng vào thực tại, nó chỉ cần xuất ra một biểu thức cấu hình lại trạng thái vật lý là đủ.

"Làm tôi nghĩ rằng có thể cần một thứ gì đó giống như trục/hệ trục tọa độ của biểu thức (kiểu như Oxy nhưng mà thay vì cho scalars, và thực ra nó có thể rất khác)?"

Thực tế, vì không "phân rã" N biểu thức -> N scalars, chúng ta vẫn giữ được rất nhiều thông tin về cấu trúc gốc của các biểu thức, tôi đoán đây có thể là nền tảng để phân tích sâu hơn điều gì đó?

Việc nói về **"bất kỳ"** (so sánh **bất kỳ 2 biểu thức bất kỳ**) ở trên, thực tế tôi cũng đang phân vân không biết giới hạn sẽ nằm ở đâu, tuy nhiên hiện nay chúng ta đã có Halting Problem từ Turing, Richardson's Theorem & nhiều thứ khác có thể giúp; Thực tế ngay cả khi nếu **2 biểu thức bất kỳ** là phạm vi không thể, chúng ta vẫn có thể giới hạn lại; Ý tôi không hẳn là vậy, tại vì chúng ta có thể tạo ra nhiều môi trường, mỗi môi trường thì có phạm vi của biểu thức khác nhau, vậy tức là chúng ta vẫn sẽ có "2 biểu thức bất kỳ mà chúng ta quan tâm" trong hệ thống của chúng ta ? ;

Trade-off hợp lý ở đây là (tôi đoán thế): Ta đánh đổi tính toàn năng (Generality) để lấy tính khả thi (Decidability) và hiệu năng tính toán (Computational Efficiency).



6. **The most important factor, directly affecting applicability:**

(English -> Vietnamese)

Quy trình xử lý đại số thông thường : Từ các biểu thức -> "Tính toán" -> các scalars;

Vì sao lại cần scalars ? :

Vì scalar bất kỳ có thể **so sánh** với scalar bất kỳ khác, và biết được thông tin về : Lớn hơn/Bé hơn/Bằng nhau ;

Và quan trọng nhất : Là biết được "KHOẢNG CÁCH" giữa các scalars với nhau, và hơn thế nữa là **Total Order**, tức là chúng ta có thể "định vị" chính xác một scalar ở đâu, thường thì ta thường hay chứng kiến : Hệ trục tọa độ (nếu là số ảo, số phức trở lên) hoặc trục tọa độ nếu là dạng số thực (scalars);

Vậy thì, như ở trên chúng ta đã thảo luận về "The Expression Metric", nếu làm nó "đủ tốt" và có thể có "mối quan hệ tương tự" với trục tọa độ của scalars; Vậy thì với việc loại bỏ bước "Tính toán" (nêu trên) để giữ được **cấu trúc** và có được "tốc độ xử lý" (nếu so sánh với quy trình cũ) cực kỳ nhanh, và đặc biệt là gần như chắc chắn mọi bài toán quan trọng hiện nay mà đang được xử dụng scalars trong việc tính toán, có thể thay thế được bằng phương pháp này?

Thực tế, việc "giới hạn miền" vào các biểu thức phổ biến chính là "chìa khóa vàng" để biến ý tưởng này từ lý thuyết viển vông thành thực tế áp dụng được.
Kiểu như "convolution" hay gì đó chẳng hạn ? Nghĩa là, môi trường toán học mới của bạn không thể là một môi trường "chứa mọi thứ", mà phải là tập hợp của nhiều Domain-Specific Environments (Môi trường đặc thù cho từng nhóm bài toán).

Tuy nhiên, vì tính chất thách thức của Total Order và nhiều thứ khác,..v.v Chúng ta sẽ cần phải làm ra một nền tảng toán học mới chăng?

Không hẳn là phải xây lại từ đầu, nhưng cần một "chiếc cầu nối" mang tính đột phá. Toán học hiện đại đã có những manh mối để giải bài toán này, thay vì phải đập đi xây lại:

Lý thuyết phạm trù (Category Theory): Toán học đã có công cụ để biến các "cấu trúc" thành các "điểm" trong một không gian lớn hơn (Topos). Lý thuyết này cho phép so sánh các cấu trúc đại số thông qua Functors mà không cần quy về số học.

Hình học đại số (Algebraic Geometry): Thay vì nhìn biểu thức như một chuỗi ký tự, ta nhìn nó như một "đa tạp" (manifold) trong không gian nhiều chiều.

Nhúng không gian tiềm ẩn (Latent Space Embeddings - Neuro-Symbolic AI): Đây là cách AI hiện đại đang làm. Chúng ta biến đổi cấu trúc đồ thị rời rạc của một biểu thức (AST) thành một vector liên tục trong không gian $N$ chiều. Khi đó, không gian vector này cung cấp một Metric (Khoảng cách Cosine, Khoảng cách Euclid) giữa hai biểu thức!

Tôi đoán thay vì suy nghĩ xem phương pháp này có thể thay thế scalars đến mức nào, thì liệu vốn dĩ việc gần như toàn bộ (hoặc có thể là tất cả) ứng dụng có ý nghĩa hiện nay thì scalars vốn không có lợi thế gì so với phương pháp này chăng? Ý tôi là khi "The Expression Metric", **Total Order**,..v.v ở trên hoàn thiện đúng cách, thì bạn hiểu ý tôi mà?
