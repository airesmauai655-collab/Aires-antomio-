<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JNJH Shop</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #f7f7f7, #e0f2f1);
      margin: 0;
      padding: 0;
      color: #333;
    }

    header {
      background-color: #00796b;
      color: white;
      text-align: center;
      padding: 30px 10px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
    }

    main {
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 40px 10px;
    }

    .produto {
      background-color: white;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      max-width: 400px;
      padding: 25px;
      text-align: center;
      margin-bottom: 30px;
    }

    img {
      width: 100%;
      border-radius: 10px;
      margin-bottom: 20px;
    }

    h2 {
      color: #00796b;
    }

    .preco {
      font-size: 1.5em;
      font-weight: bold;
      color: #004d40;
    }

    button {
      background-color: #00796b;
      color: white;
      border: none;
      padding: 12px 25px;
      border-radius: 8px;
      font-size: 16px;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background-color: #004d40;
    }

    footer {
      text-align: center;
      padding: 20px;
      background-color: #004d40;
      color: white;
      font-size: 14px;
    }
  </style>
</head>
<body>

  <header>
    <h1>JNJH Shop</h1>
    <p>Conhecimento que transforma!</p>
  </header>

  <main>
    <div class="produto">
      <img src="https://picsum.photos/400/250" alt="Imagem do produto">
      <h2>JMJH Curso Online</h2>
      <p>Conhecimento que transforma! Acesse conteúdo exclusivo com <strong>direito PLR</strong>: aprenda, use e revenda. Invista em você e crie sua própria renda. <em>Comece agora!</em></p>
      <p class="preco">💰 1.580 MT</p>
      <a href="https://wa.me/258869644130?text=Olá! Quero comprar o JMJH Curso Online por 1580MT.">
        <button>Comprar no WhatsApp</button>
      </a>
    </div>
  </main>

  <footer>
    &copy; 2025 JNJH Shop — Todos os direitos reservados
  </footer><!-- ======= Formas de Pagamento ======= -->
<section id="pagamentos" style="text-align:center;margin:50px 0;padding:20px;background:#f5f7f6;border-radius:12px;">
  <h2 style="color:#00796b;">💳 Formas de Pagamento</h2>
  <p style="font-size:1rem;color:#333;">Escolhe o método que preferes para pagar:</p>

  <div style="display:flex;flex-direction:column;align-items:center;gap:20px;max-width:400px;margin:auto;">

    <!-- PayPal -->
    <a href="#" style="background:#0070ba;color:#fff;padding:12px 18px;border-radius:8px;text-decoration:none;width:100%;text-align:center;font-weight:bold;">
      💳 Pagar com PayPal (Demo)
    </a>

    <!-- M-Pesa -->
    <a href="#" style="background:#4caf50;color:#fff;padding:12px 18px;border-radius:8px;text-decoration:none;width:100%;text-align:center;font-weight:bold;">
      📱 Pagar com M-Pesa (Demo)
    </a>

    <!-- E-Mola -->
    <a href="#" style="background:#ff9800;color:#fff;padding:12px 18px;border-radius:8px;text-decoration:none;width:100%;text-align:center;font-weight:bold;">
      💰 Pagar com E-Mola (Demo)
    </a>
  </div>

  <!-- Espaço para Imagens (ex: logotipos ou QR codes) -->
  <div style="margin-top:30px;">
    <img src="https://upload.wikimedia.org/wikipedia/commons/b/b5/PayPal.svg" alt="PayPal" style="height:50px;margin:10px;">
    <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/Mpesa-logo.png" alt="M-Pesa" style="height:50px;margin:10px;">
    <img src="https://upload.wikimedia.org/wikipedia/commons/d/d3/EMola_logo.png" alt="E-Mola" style="height:50px;margin:10px;">
  </div>

  <div style="margin-top:25px;">
    <a href="https://wa.me/258869644130?text=Olá!%20Preciso%20de%20ajuda%20com%20o%20pagamento"
       style="color:#00796b;text-decoration:underline;font-weight:bold;">💬 Falar com suporte no WhatsApp</a>
  </div>
</section>
<!-- ======= /Fim das Formas de Pagamento ======= -->

<!-- ======= Upload e Pré-visualização de Imagens ======= -->
<section id="image-uploader" style="max-width:760px;margin:30px auto;padding:18px;background:#fff;border-radius:12px;box-shadow:0 6px 18px rgba(0,0,0,0.06);text-align:center;">
  <h2 style="color:#00796b;margin-top:0;">📷 Adicionar imagens</h2>
  <p style="color:#333;margin-bottom:8px;">Arrasta e larga ou clica para seleccionar imagens. Pré-visualização imediata.</p>

  <div id="drop-area" style="border:2px dashed #cfeee9;padding:18px;border-radius:10px;cursor:pointer;background:#f9fffd;">
    <input id="fileElem" type="file" accept="image/*" multiple style="display:none">
    <div style="font-size:0.95rem;color:#00695c;">
      <strong>Clica ou arrasta imagens aqui</strong><br>
      (jpg, png, gif — até 5 MB por imagem)
    </div>
  </div>

  <div id="gallery" style="display:flex;flex-wrap:wrap;gap:12px;justify-content:center;margin-top:18px;"></div>

  <div style="margin-top:14px;">
    <button id="clear-images" style="background:#ff7043;color:#fff;border:none;padding:8px 12px;border-radius:8px;cursor:pointer">Remover todas</button>
  </div>
</section>

<script>
(function(){
  const MAX_SIZE_MB = 5;
  const drop = document.getElementById("drop-area");
  const fileElem = document.getElementById("fileElem");
  const gallery = document.getElementById("gallery");
  const clearBtn = document.getElementById("clear-images");
  const STORAGE_KEY = "jnjh_uploaded_images_v1";

  // carregar do localStorage
  let images = JSON.parse(localStorage.getItem(STORAGE_KEY) || "[]");
  renderGallery();

  // eventos
  drop.addEventListener("click", ()=> fileElem.click());
  fileElem.addEventListener("change", (e)=> handleFiles(e.target.files));
  ;["dragenter","dragover"].forEach(evt => drop.addEventListener(evt, (e)=> { e.preventDefault(); drop.style.background="#eafff6"; }));
  ;["dragleave","drop"].forEach(evt => drop.addEventListener(evt, (e)=> { e.preventDefault(); drop.style.background="#f9fffd"; }));
  drop.addEventListener("drop", (e)=> {
    const dt = e.dataTransfer;
    if(dt && dt.files) handleFiles(dt.files);
  });

  clearBtn.addEventListener("click", ()=>{
    if(!confirm("Remover todas as imagens da galeria?")) return;
    images = [];
    saveAndRender();
  });

  function handleFiles(files){
    const list = Array.from(files);
    list.forEach(file => {
      if(!file.type.startsWith("image/")) return alert("Apenas imagens são permitidas.");
      if(file.size > MAX_SIZE_MB * 1024 * 1024) return alert(`Imagem muito grande. Máx: ${MAX_SIZE_MB} MB.`);
      const reader = new FileReader();
      reader.onload = (ev) => {
        images.push({dataUrl: ev.target.result, name: file.name, size: file.size});
        saveAndRender();
      };
      reader.readAsDataURL(file);
    });
    fileElem.value = ""; // limpa input
  }

  function renderGallery(){
    gallery.innerHTML = "";
    if(images.length === 0){
      gallery.innerHTML = `<div style="color:#666;padding:18px">Nenhuma imagem adicionada.</div>`;
      return;
    }
    images.forEach((img, idx) => {
      const div = document.createElement("div");
      div.style = "width:150px;border-radius:10px;overflow:hidden;background:#fff;border:1px solid #eee;box-shadow:0 4px 10px rgba(0,0,0,0.04);";
      div.innerHTML = `
        <div style="height:110px;display:flex;align-items:center;justify-content:center;background:#fafafa">
          <img src="${img.dataUrl}" alt="${escapeHtml(img.name)}" style="max-width:100%;max-height:100%;object-fit:cover;display:block">
        </div>
        <div style="padding:8px;font-size:0.85rem;color:#333;text-align:left;">
          <div style="font-weight:700;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;">${escapeHtml(img.name)}</div>
          <div style="font-size:0.8rem;color:#666;margin-top:6px;display:flex;gap:6px;justify-content:space-between;align-items:center">
            <span>${(img.size/1024|0)} KB</span>
            <div>
              <button data-idx="${idx}" class="use-btn" style="background:#00796b;color:#fff;border:none;padding:4px 8px;border-radius:6px;cursor:pointer;font-size:0.78rem">Usar</button>
              <button data-idx="${idx}" class="del-btn" style="background:#e0e0e0;color:#333;border:none;padding:4px 8px;border-radius:6px;cursor:pointer;font-size:0.78rem;margin-left:6px">Eliminar</button>
            </div>
          </div>
        </div>
      `;
      gallery.appendChild(div);
    });

    // ligar eventos dos botões
    gallery.querySelectorAll(".del-btn").forEach(b=>{
      b.addEventListener("click", ()=> {
        const i = Number(b.getAttribute("data-idx"));
        images.splice(i,1);
        saveAndRender();
      });
    });
    gallery.querySelectorAll(".use-btn").forEach(b=>{
      b.addEventListener("click", ()=>{
        const i = Number(b.getAttribute("data-idx"));
        // exemplo: abre a imagem numa nova aba ou podes inserir no site conforme precisares
        const w = window.open();
        w.document.write('<title>Imagem</title><img src="'+images[i].dataUrl+'" style="max-width:100%;height:auto;display:block;margin:20px auto">');
      });
    });
  }

  function saveAndRender(){
    try {
      localStorage.setItem(STORAGE_KEY, JSON.stringify(images));
    } catch(e){
      console.warn("Não foi possível salvar no localStorage:", e);
    }
    renderGallery();
  }

  // util
  function escapeHtml(s){ return String(s).replace(/[&<>"']/g, m => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[m])); }
})();
</script>
<!-- ======= /Fim Upload ======= -->

</body>
</html>
import React, {useEffect,useState} from 'react';
import axios from 'axios';
export default function Home(){
  const [products,setProducts] = useState([]);
  useEffect(()=>{ axios.get('/api/products').then(r=>setProducts(r.data)).catch(()=>{}); },[]);

  const mpesaNumber = '858477539';
  const molaNumber = '869644130';

  return <div>
    <section style={{display:'flex',gap:20,alignItems:'center',marginBottom:20}}>
      <div style={{flex:1}}>
        <h2>Bem-vindo à JNJH</h2>
        <p>Plataforma de venda de produtos digitais — pagamento rápido por M-Pesa, Mola ou PayPal.</p>
        <div style={{marginTop:12,padding:12,border:'1px solid #eee',borderRadius:8,background:'#fafafa'}}>
          <h4>Formas de pagamento</h4>
          <ul>
            <li><strong>M-Pesa:</strong> Envia para <code>{mpesaNumber}</code> e contacta o suporte após pagamento.</li>
            <li><strong>Mola:</strong> Envia para <code>{molaNumber}</code> e confirma o pagamento.</li>
            <li><strong>PayPal:</strong> Paga pelo checkout online (Stripe/PayPal/MPesa integrados).</li>
          </ul>
          <small>Após receber a confirmação automática via webhook, o link de download será enviado ao e-mail do comprador.</small>
        </div>
      </div>
      <div style={{width:180}}>
        <img src='/logo.png' alt='logo' style={{width:'100%',borderRadius:8}}/>
      </div>
    </section>

    <section>
      <h3>Produtos</h3>
      {products.length===0? <p>Nenhum produto (start backend)</p> : products.map(p=>(
      <div key={p._id} style={{border:'1px solid #ddd',padding:12,marginBottom:8}}>
        <h4>{p.title} — R$ {(p.priceCents/100).toFixed(2)}</h4>
        <p>{p.description}</p>
        <div style={{display:'flex',gap:8}}>
          <button onClick={async ()=>{
            const affiliateCode = prompt('Se és afiliado, coloca o teu código (ou cancela)');
            try{
              const res = await axios.post('/api/checkout/create-session', { productId: p._id, buyerEmail: 'cliente@exemplo.com', affiliateCode });
              alert('Session criada (frontend demo). Vai pagar usando a Stripe/PayPal/Mobile Money configurada no backend.');
            }catch(err){ alert('Erro: ' + (err.response?.data?.error || err.message)); }
          }}>Comprar (Checkout)</button>

          <button onClick={()=>{
            alert('Para pagar por M-Pesa: envia para ' + mpesaNumber + '.\\nPara pagar por Mola: envia para ' + molaNumber + '.\\nDepois confirma o pagamento no suporte ou aguarda confirmação automática.');
          }}>Pagar por M-Pesa / Mola</button>
        </div>
        <div style={{marginTop:6}}>
          <small>Link de afiliado exemplo: <code>{window.location.origin + '/product/' + p._id + '?ref=SEUCOD'}</code></small>
        </div>
      </div>
    ))}</section>
  </div>;
}
