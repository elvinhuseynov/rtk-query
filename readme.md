Yenilənmiş tapşırıq: 
-- https://jsonplaceholder.typicode.com/users Api yaratmalı və buradan gələn datanı /users adlı yeni bir route yaradaraq göstərməlisiniz.
-- Hər hansı bir user-ə clicklədikdə, /users/:id adlı yeni yaradacağınız route-a yönləndirməlisiniz.
-- Və bu Route-da https://jsonplaceholder.typicode.com/users/:id adlı yeni yaradacağınız api requestindən gələn datanı göstərməlisiniz.
Keçən dərsə aid tapşırıqdan istifadə edin!





Keçən dərsə aid tapşırıqdan:

1. **Layihənin Qurulması:**
   - Yeni bir React layihəsi yaradın.
   - Aşağıdakı library-ləri quraşdırın:
     - `zustand`
     - `@reduxjs/toolkit`
     - `@chakra-ui/react`
     - `@emotion/react`
     - `@emotion/styled`
     - `framer-motion`
     - `react-router`

2. **RTK Query ilə Data Çəkmə:**
   - RTK Query istifadə edərək bir API slice yaradın və aşağıdakı endpoint-ləri əlavə edin:
     - `https://jsonplaceholder.typicode.com/posts` ünvanından postların siyahısını çəkmək.
     - `https://jsonplaceholder.typicode.com/comments?postId={postId}` ünvanından seçilmiş post üçün şərhləri çəkmək.
   - RTK Query-dən yalnız API sorğuları üçün istifadə edin; tətbiqin vəziyyətini RTK Query vasitəsilə idarə etməyin.

3. **Zustand ilə State İdarəsi:**
   - Global state idarə etmək üçün Zustand store yaradın və aşağıdakı məlumatları saxlayın:
     - Postların siyahısı.
     - Seçilmiş post.
     - Postları axtarmaq/filtrləmək üçün axtarış meyarları.
   - RTK Query vasitəsilə postlar çəkildikdə, onları Zustand store-a daxil edin.
   - Post seçildikdə, Zustand store-u yeniləyin.

4. **Chakra UI ilə İstifadəçi İnterfeysi:**
   - Chakra UI komponentlərindən istifadə edərək interfeysi yaradın.
   - Əsas görünüşdə postların siyahısı göstərilməlidir; hər post üçün başlıq və qısa məlumat yer almalıdır.
   - Postların başlığına görə filtrləmə üçün axtarış/filtr qutusu əlavə edin.
   - İstifadəçi bir posta kliklədikdə, detallı görünüş göstərilsin:
     - Postun tam mətni.
     - Posta aid şərhlərin siyahısı.
   - İstifadəçi interfeysi cavabverici və əlçatan olmalıdır.

5. **Tətbiqin Funksionallığı:**
   - Tətbiq yükləndikdə, RTK Query vasitəsilə postların siyahısını çəkin və onları Zustand store-a əlavə edin.
   - İstifadəçi axtarış/filtr vasitəsilə postları filtrləyə bilsin.
   - İstifadəçi bir posta kliklədikdə, Zustand store-da seçilmiş postu yeniləyin və onun şərhlərini RTK Query ilə çəkin və daha sonra həmin səhifəyə react router ilə keçid edin.
