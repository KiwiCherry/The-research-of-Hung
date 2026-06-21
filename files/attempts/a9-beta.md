
(vietnamese)

**Authors:** Hung Dinh Phu Dang  

**Date:** 17-18, June 2026  


Thay vì : "Làm sao để tính ra N đáp án vô hướng của N biểu thức nhanh nhất?" ; Thì : "Tại sao phải cần đáp án vô hướng trong khi ta chỉ cần ý nghĩa về mối quan hệ và khả năng "Total Order" (LƯU Ý RẰNG TÔI ĐÃ CHÈN DẤU NGOẶC KÉP VÀO!) của chúng?"

và "Liệu hầu như TẤT CẢ những bài toán quan trọng hiện nay về bản chất không thực sự cần scalar hay không?" ;

"Nếu tạo ra một nền tảng & môi trường trong khuôn khổ chặt chẽ và logic, nơi mà tự động N biểu thức có mối quan hệ tương tự với N scalars (nếu áp dụng trên máy tính điện tử truyền thống, phải là O(1)), từ đó việc tính toán ra N scalars là vô nghĩa (trên máy tính điện tử truyền thống là : O(n) ) ; Thiết kế chặt chẽ để các trade-off là hợp lý để không thành 'rác' lý thuyết" ;


Chỉ cần lý thuyết này có thể so sánh **bất kỳ 2 biểu thức bất kỳ** với nhau (< ; > ; =) và biết được "khoảng cách (na ná giống kiểu Total Order)" (LƯU Ý RẰNG TÔI ĐÃ CHÈN DẤU NGOẶC KÉP VÀO!) giữa chúng tương tự như scalars,  và các trade-off là hợp lý để không thành 'rác' lý thuyết, đây có thể là thứ chúng ta đang tìm?



Thực tế, vì không "phân rã" N biểu thức -> N scalars, chúng ta vẫn giữ được rất nhiều thông tin về cấu trúc gốc của các biểu thức, tôi đoán đây có thể là nền tảng để phân tích sâu hơn điều gì đó?

Trade-off hợp lý ở đây là (tôi đoán thế): Ta đánh đổi tính toàn năng (Generality) để lấy tính khả thi (Decidability) và hiệu năng tính toán (Computational Efficiency).

Tức là chỉ có N biểu thức ở đầu vào, mà trong đó các biểu thức chỉ bao gồm các phép toán cơ bản (+;-;*;:) và số thực với "độ phân giải hữu hạn", không bao gồm các hàm siêu việt như sin, exp, log,.. ;


**The most important factor, directly affecting applicability:**

(English -> Vietnamese)

Quy trình xử lý đại số thông thường : Từ các biểu thức -> "Tính toán" -> các scalars;



Vậy thì, như ở trên chúng ta đã thảo luận, nếu làm nó "đủ tốt" và có thể có "mối quan hệ" và "Total Order" với trục tọa độ của scalars; Vậy thì với việc loại bỏ bước "Tính toán" (nêu trên) để giữ được **cấu trúc** và có được "tốc độ xử lý" (nếu so sánh với quy trình cũ trên máy tính điện tử) cực kỳ nhanh, và đặc biệt là gần như chắc chắn mọi bài toán quan trọng hiện nay mà đang được xử dụng scalars trong việc tính toán, có thể thay thế được bằng phương pháp này?

Tuy nhiên, vì tính chất thách thức của "Total Order" và nhiều thứ khác,..v.v Chúng ta sẽ cần phải làm ra một nền tảng toán học mới chăng?

Tôi đoán thay vì suy nghĩ xem phương pháp này có thể thay thế scalars đến mức nào, thì liệu vốn dĩ việc gần như toàn bộ (hoặc có thể là tất cả) ứng dụng có ý nghĩa hiện nay thì scalars vốn không có lợi thế gì so với phương pháp này chăng? Ý tôi là khi "mối quan hệ", **Total Order**,..v.v ở trên hoàn thiện đúng cách, thì bạn hiểu ý tôi mà?

===

Core Research Question :

Rather than asking "How do we compute N scalar answers from N expressions as fast as possible?", we propose asking: "Why do we need scalar outputs when relational structure and total orderings between expressions suffice?"

Primary Hypothesis: ALL contemporary important problems do not fundamentally require scalar decomposition. (If it's considered mandatory to have scalars, then it's an illusion.)

Proposed Framework :

Central Idea :

Construct a mathematically rigorous formal system where:

N symbolic expressions maintain structural integrity (no decomposition into scalars)

Automatic extraction of relational structure that corresponds bijectively to scalar relationships

Computational cost: far superior to O(n) scalar computation (traditional systems)

Key Properties Required :

Comparability: Any two arbitrary expressions must be comparable using {<, >, =}

Distance metric: Define a "distance" or "gap" between expressions analogous to scalar spacing

Decidability: Computable comparisons with polynomial-time bounds

Decidability: Rational trade-offs preventing theoretical vacuousness

The Preservation Advantage :

By avoiding expression-to-scalar decomposition, we retain structural information about the original expressions. This preserved structure may enable deeper analysis of expression relationships and properties.


Computational Trade-Off :

We propose exchanging generality for decidability and efficiency:

Input Restriction:

N expressions containing only:

Basic arithmetic operations: {+, −, ×, ÷}

Real numbers with finite precision

Exclusions: Transcendental functions (sin, exp, log, etc.)

The Fundamental Question :

Current Approach

Expressions → Computation → Scalar values

Proposed Approach

Expressions → Relational Structure (preserving all ordering/distance properties of scalar equivalents) → Direct analysis at reduced computational cost

The Key Insight :

Rather than ask "To what extent can this method replace scalars?", we should ask: "Do meaningful contemporary applications actually gain any advantage from scalar decomposition when relational structure & "distance" is properly formalized?"



In other words: when relational properties, total orderings, and distance metrics are correctly developed, don't scalars become computationally redundant?

Challenges & Requirements :

This approach requires developing new mathematical foundations to rigorously handle:

Total ordering on non-scalar objects

Distance/metric properties without explicit coordinate systems

Decidability proofs for the comparison framework

Integration with existing problem domains currently formulated in scalar arithmetic


Expected Outcome :

A foundational mathematical system enabling expression-native computation at speed and decidability to exceeding scalar-based approaches, while preserving structural information lost in traditional decomposition.


