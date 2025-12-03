<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>BEAT SMASHERS</title>
  <style>
    :root{
      --accent:#ff2d95;
      --dark:#0f0f14;
      --muted:#9aa1ad;
      --card:#121217;
      --glass: rgba(255,255,255,0.04);
      --maxw:1100px;
      --radius:12px;
      font-family: Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
    }
    *{box-sizing:border-box}
    body{margin:0;background:linear-gradient(180deg,#07070b 0%, #0b0b10 100%);color:#e8eef8;line-height:1.45}
    .container{max-width:var(--maxw);margin:28px auto;padding:20px}
    header{display:flex;align-items:center;justify-content:space-between;gap:12px}
    .brand{display:flex;align-items:center;gap:12px}
    .logo{width:64px;height:64px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#6b3bff);display:flex;align-items:center;justify-content:center;font-weight:700}
    nav a{color:var(--muted);text-decoration:none;margin-left:18px}
    nav a:hover{color:var(--accent)}

    .hero{display:grid;grid-template-columns:1fr 380px;gap:28px;align-items:center;margin-top:28px}
    .hero h1{font-size:36px;margin:0}
    .hero p{color:var(--muted);margin-top:8px}
    .cta{margin-top:18px}
    .btn{background:var(--accent);border:none;padding:10px 16px;border-radius:10px;color:white;cursor:pointer}

    /* Player card */
    .player{background:var(--card);padding:18px;border-radius:14px;box-shadow:0 6px 20px rgba(0,0,0,0.6)}
    .track-list{margin-top:12px}
    .track{display:flex;align-items:center;justify-content:space-between;padding:8px;border-radius:8px;cursor:pointer}
    .track:hover{background:var(--glass)}

    /* Sections */
    section{margin-top:36px}
    h2{margin:0 0 12px 0}

    /* Tour table */
    table{width:100%;border-collapse:collapse}
    th,td{padding:10px;text-align:left;border-bottom:1px solid rgba(255,255,255,0.04)}
    .buy-btn{background:transparent;border:1px solid var(--accent);padding:6px 10px;border-radius:8px;color:var(--accent);cursor:pointer}

    /* Merch */
    .merch-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:16px}
    .card{background:linear-gradient(180deg,rgba(255,255,255,0.02),rgba(255,255,255,0.01));padding:12px;border-radius:12px}
    .price{font-weight:700}

    /* Gallery */
    .gallery-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:12px}
    .media{border-radius:8px;overflow:hidden}
    img{display:block;width:100%;height:200px;object-fit:cover}

    /* Footer */
    footer{margin-top:36px;padding:18px;border-top:1px solid rgba(255,255,255,0.03);color:var(--muted);display:flex;justify-content:space-between;align-items:center}

    /* Responsive */
    @media (max-width:900px){
      .hero{grid-template-columns:1fr}
      .hero .player{order:-1}
      img{height:140px}
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">NE</div>
        <div>
          <div style="font-weight:700">BEAT SMASHERS</div>
          <div style="font-size:13px;color:var(--muted)">Alt‑electro / Live band</div>
        </div>
      </div>
      <nav>
        <a href="#music">Music</a>
        <a href="#tour">Tour</a>
        <a href="#merch">Merch</a>
        <a href="#gallery">Gallery</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>

    <main>
      <div class="hero">
        <div>
          <h1>Feel the BEAT. SMASH the music.</h1>
          <p>Official site of BEAT SMASHERS — immersive live shows, new singles, and touring worldwide. Join our mailing list for early presale access.</p>
          <div class="cta">
            <button class="btn" onclick="document.getElementById('music').scrollIntoView({behavior:'smooth'})">Listen Now</button>
            <button class="btn" style="background:transparent;border:1px solid rgba(255,255,255,0.06);margin-left:8px">Subscribe</button>
          </div>
        </div>

        <aside class="player">
          <strong>Now playing</strong>
          <div id="now" style="margin-top:8px;color:var(--muted)">—</div>

          <audio id="audio" controls style="width:100%;margin-top:12px">
            <source id="source" src="" type="audio/mpeg">
            Your browser does not support audio.
          </audio>

          <div class="track-list" id="tracks">
            <!-- Tracks injected by JS -->
          </div>
          <div style="margin-top:10px;color:var(--muted);font-size:13px">Tip: click a track to play</div>
        </aside>
      </div>

      <section id="music">
        <h2>Latest Releases</h2>
        <p style="color:var(--muted);margin-top:6px">Stream our newest singles and the upcoming EP.</p>
        <!-- simple release list -->
        <div style="display:flex;gap:12px;margin-top:12px;flex-wrap:wrap">
          <div class="card" style="min-width:220px;flex:1">
            <div style="font-weight:700">Neon Night (Single)</div>
            <div style="color:var(--muted);margin-top:6px">Released: Oct 8, 2025</div>
            <div style="margin-top:8px">A synth-driven anthem built for late-night rooftops.</div>
          </div>
          <div class="card" style="min-width:220px;flex:1">
            <div style="font-weight:700">Echoes EP (Pre-order)</div>
            <div style="color:var(--muted);margin-top:6px">Release: Jan 15, 2026</div>
            <div style="margin-top:8px">Four tracks exploring analog textures and live drums.</div>
          </div>
        </div>
      </section>

      <section id="tour">
        <h2>Tour Dates</h2>
        <p style="color:var(--muted)">Catch us live — more dates added weekly.</p>
        <div style="margin-top:12px;overflow:auto;background:var(--card);padding:12px;border-radius:10px">
          <table>
            <thead>
              <tr><th>Date</th><th>City / Venue</th><th>Tickets</th></tr>
            </thead>
            <tbody id="tour-list">
              <!-- tour rows inserted by JS -->
            </tbody>
          </table>
        </div>
      </section>

      <section id="merch">
        <h2>Merch Store</h2>
        <p style="color:var(--muted)">Official shirts, vinyl, and limited posters.</p>
        <div class="merch-grid" style="margin-top:12px">
          <div class="card">
            <img src="https://via.placeholder.com/400x300?text=T-Shirt" alt="tshirt" style="width:100%;height:140px;object-fit:cover;border-radius:8px">
            <div style="margin-top:8px">Neon Echo Tee</div>
            <div class="price">₹999</div>
            <div style="margin-top:8px"><button class="buy-btn" onclick="addToCart('Neon Echo Tee',999)">Add to cart</button></div>
          </div>

          <div class="card">
            <img src="https://via.placeholder.com/400x300?text=Vinyl" alt="vinyl" style="width:100%;height:140px;object-fit:cover;border-radius:8px">
            <div style="margin-top:8px">Echoes (Vinyl)</div>
            <div class="price">₹1499</div>
            <div style="margin-top:8px"><button class="buy-btn" onclick="addToCart('Echoes (Vinyl)',1499)">Add to cart</button></div>
          </div>

          <div class="card">
            <img src="https://via.placeholder.com/400x300?text=Poster" alt="poster" style="width:100%;height:140px;object-fit:cover;border-radius:8px">
            <div style="margin-top:8px">Limited Poster</div>
            <div class="price">₹499</div>
            <div style="margin-top:8px"><button class="buy-btn" onclick="addToCart('Limited Poster',499)">Add to cart</button></div>
          </div>
        </div>
      </section>

      <section id="gallery">
        <h2>Gallery</h2>
        <p style="color:var(--muted)">Photos & Videos from recent shows.</p>
        <div class="gallery-grid" style="margin-top:12px">
          <div class="media"><img src="https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.rollingstone.com%2Fmusic%2Fmusic-news%2Fthe-neighbourhood-reunites-after-hiatus-drummer-firing-1235419132%2F&psig=AOvVaw2THPNFjL35KqxQJ5v7Xnf0&ust=1764876896938000&source=images&cd=vfe&opi=89978449&ved=0CBUQjRxqFwoTCOCupveUopEDFQAAAAAdAAAAABAE" alt="live1"></div>
          <div class="media"><img src=https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ5WvD6pFgGieHUtKgM5MOWObG8Ore7RqCV9Q&s" alt="backstage"></div>
          <div class="media"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRDo7_vdFe99MyhRA53WoAM942lWQ0jJ-RWGQ&s" alt="crowd"></div>
          <div class="media"><iframe width="100%" height="200" src="https://www.youtube.com/embed/dQw4w9WgXcQ" title="Video" frameborder="0" allowfullscreen></iframe></div>
        </div>
      </section>

      <section id="contact">
        <h2>Contact & Booking</h2>
        <p style="color:var(--muted)">For bookings and press: <strong>bookings@neonecho.example</strong></p>
      </section>

    </main>

    <footer>
      <div>© Neon Echo — 2025</div>
      <div style="color:var(--muted)">Follow us on social media • Instagram • Twitter • YouTube</div>
    </footer>
  </div>

  <script>
    // --- Dummy data for tracks and tour ---
    const tracks = [
      {title:'Neon Night', src:'https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3'},
      {title:'Midnight Drive', src:'https://www.soundhelix.com/examples/mp3/SoundHelix-Song-2.mp3'},
      {title:'Echo Chamber', src:'https://www.soundhelix.com/examples/mp3/SoundHelix-Song-3.mp3'},
    ];

    const tour = [
      {date:'2025-12-15',city:'Mumbai, IN',venue:'Blue Orchid',tickets:'#'},
      {date:'2026-01-10',city:'Bengaluru, IN',venue:'Skyline Arena',tickets:'#'},
      {date:'2026-02-05',city:'London, UK',venue:'The Roundhouse',tickets:'#'},
    ];

    const tracksContainer = document.getElementById('tracks');
    const audio = document.getElementById('audio');
    const source = document.getElementById('source');
    const now = document.getElementById('now');

    function renderTracks(){
      tracks.forEach((t,i)=>{
        const div = document.createElement('div');
        div.className='track';
        div.innerHTML = `<div>${i+1}. ${t.title}</div><div style=font-size:13px;color:var(--muted)>play</div>`;
        div.onclick = ()=>{ playTrack(i) };
        tracksContainer.appendChild(div);
      })
    }

    function playTrack(i){
      source.src = tracks[i].src;
      audio.load();
      audio.play();
      now.textContent = tracks[i].title;
    }

    function renderTour(){
      const tbody = document.getElementById('tour-list');
      tour.forEach(t=>{
        const tr = document.createElement('tr');
        tr.innerHTML = `<td>${t.date}</td><td>${t.city} — ${t.venue}</td><td><button class='buy-btn' onclick="alert('Redirect to ticket page for ${t.city}')">Buy</button></td>`;
        tbody.appendChild(tr);
      })
    }

    function addToCart(item,price){
      alert(item + ' added to cart — ₹' + price + '. (Demo cart)');
    }

    // init
    renderTracks();
    renderTour();

    // autoplay first track for demo (comment out if undesired)
    // playTrack(0);
  </script>
</body>
</html>
