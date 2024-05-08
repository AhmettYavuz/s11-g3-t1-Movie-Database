Daha önce bir şirket için Movie Database uygulaması yapmıştın. Yeni versiyonunu hazırlamak istiyorlar. İlgili şirket ile toplantı yaparak isterleri aldın ve iş listesini çıkardın. Kolay gelsin.

ADIM 1: Film Düzenleme:
[ ] App.jsx içinde film EditMovieForm.jsx componentini yeni bir route ile ekle: /movies/edit/:id
[ ] EditMovieForm.jsxde idyi useParams hooku ile al.
[ ] Component mount olduğunda ilgili filmin bilgisini apiden GET isteği ile al ve movie stateine aktar: https://nextgen-project.onrender.com/api/s11d3/movies/:id
[ ] Düzenleme formu submit edildiğinde çalışmıyor. Gerekli api isteğini ekle: PUT https://nextgen-project.onrender.com/api/s11d3/movies/:id
[ ] Apiden gelen tüm filmler verisini movies stateine gönder ve sayfayı ilgili filmin detay sayfasına yönlendir. /movies/:id
ADIM 2: Film Silme:
[ ] App.jsx içindeki deleteMovie fonksiyonunu film silme isteği yapacak şekilde tamamla.
[ ] Filmi silmek için ilgili Api isteğini at: DELETE https://nextgen-project.onrender.com/api/s11d3/movies/:id
[ ] responseda gelen dataya göre movies stateini güncelle.
[ ] bu fonksiyonu Movie componentine gönder.
[ ] Movie.jsxde sil butonu ekle ve bu butona event handler ekle.
[ ] Sil butonu arkplan rengini bg-red-600 yap. hover ve dark mode için uygun renkleri diğer butonlardan örnek alarak yap.
[ ] Bu event handlerda deleteMovie fonskiyonunu kullanarak filmi sil.
[ ] İstek tamamlandığında kullanıcıyı /movies routeuna yönlendir.
ADIM 3: Yeni Film Ekleme:
[ ] Sıfırdan "AddMovieForm" componenti oluşturmak için "EditMovieForm.jsx"i model olarak kullan.
[ ] AddMovieForm'a erişim sağlayan bir route ekle: movies/add
[ ] UIda AddMoiveForma yönlenecek butonu bul ve tıklanınca film ekleme sayfasının açılmasını sağla.
[ ] AddMovieForm'da, form submit için bir event handler ekleyin. Form submit edildiğinde, formdaki datayı POST olarak https://nextgen-project.onrender.com/api/s11d3/moviese gönder.
[ ] İstek başarılı olunca App.jsxdeki movies statini güncelle.
[ ] /movies routeuna yönlendir.
ADIM 4: Favori Özelliğini Ekle:
[ ] Favori ekle butonuna basılınca favorilere eklenmesi için gerekli işlemleri yap.
[ ] Aynı filmin 2 kere eklenmesini engelle.
[ ] Film silinince favorilerden de sil.
ADIM 4: DarkMode Özelliğini Ekle:
[ ] UIda ekli bulunan Dark mode butonunun çalışır hale getir. hooks/useLocalStorage.jsx hookunu kullanarak localstoragea s11d3 anahtarı ile darkMode statei oluştur. Başlangıç değeri true olsun.
[ ] Darkmode switchine onChange eventi ekleyerek darkMode stateini değiştir.
[ ] Darkmode On olunca App.jsxde en üstteki divin classını dark bg-slate-900 h-screen yapsın. Off olunca bu classları eklemesin.
[ ] Darkmode açık iken butonda Darkmode On yazsın, kapalı iken Darkmode Off yazsın.
[ ] Darkmode açık iken buton checked olsun.
API RESPONSE ÖRNEĞİ:
İPUCU: APIden aşağıdaki formatta filmler gelir:

[
{
id: 5,
title: 'Tombstone',
director: 'George P. Cosmatos',
metascore: 89,
genre: 'Drama',
description:
"A successful lawman's plans to retire anonymously in Tombstone, Arizona are disrupted by the kind of outlaws he was famous for eliminating.",
},
];
Çalışma dosyaları: src/components/AddMovieForm.jsx, src/components/EditMovieForm.jsx, src/components/Movie.jsx, src/App.jsx
