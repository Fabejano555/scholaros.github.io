<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>ScholarOS | A ScholarOS-based Linux Distribution</title>
  <meta name="description" content="ScholarOS - A ScholarOS-based Linux Distro" />
  <style>
    :root{--accent:#0069a8;--muted:#6b7280;--bg:#0f1724;--card:#0b1220;color-scheme: dark}
    *{box-sizing:border-box}
    html,body{height:100%}
    body{font-family:Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;line-height:1.4;margin:0;background:linear-gradient(180deg,#071427 0%, #081827 60%);color:#e6eef6;padding:24px}
    .container{max-width:960px;margin:0 auto}
    header{display:flex;align-items:center;justify-content:space-between;gap:16px}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:56px;height:56px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#0b7285);display:flex;align-items:center;justify-content:center;font-weight:700;color:white;box-shadow:0 6px 20px rgba(2,6,23,.6)}
    h1{font-size:clamp(1.4rem,3vw,2rem);margin:0}
    p.lead{color:var(--muted);margin:8px 0 0}
    nav a{color:#cfefff;text-decoration:none;margin-left:12px}
    .hero{display:grid;grid-template-columns:1fr 320px;gap:24px;margin-top:28px;align-items:start}
    .card{background:rgba(255,255,255,0.02);padding:18px;border-radius:12px;box-shadow:0 6px 18px rgba(2,6,23,.6)}
    .download{display:flex;flex-direction:column;gap:8px}
    .btn{display:inline-block;padding:10px 14px;border-radius:8px;text-decoration:none;font-weight:600}
    .btn-primary{background:linear-gradient(90deg,var(--accent),#0793c7);color:white}
    .btn-ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:#cde9ff}
    .features{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin-top:18px}
    .feature{padding:12px;border-radius:10px;background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.00));}
    .feature h3{margin:0 0 6px}
    .cli{background:#071422;padding:12px;border-radius:8px;font-family:monospace;color:#bfe7ff}
    footer{margin-top:32px;color:var(--muted);font-size:0.9rem;text-align:center}
    @media (max-width:880px){
      .hero{grid-template-columns:1fr}
      .features{grid-template-columns:1fr}
      nav{display:none}
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">SO</div>
        <div>
          <h1>ScholarOS</h1>
          <p class="lead">A Lightweight, School-Focused Linux Distribution</p>
        </div>
      </div>
      <nav>
        <a href="#features">Features</a>
        <a href="#download">Download</a>
        <a href="#about">About</a>
        <a href="#docs">Docs</a>
      </nav>
    </header>
    <main>
      <section class="hero">
        <div class="card">
          <h2>Fast. Modern. Secure.</h2>
          <p class="lead">ScholarOS combines stability with curated packages and sensible defaults for privacy, performance and developer tooling.</p>
          <div id="features" class="features">
            <div class="feature">
              <h3>GNOME & Wayland</h3>
              <p class="muted">Polished ScholarOS GNOME session on Wayland with performance tweaks.</p>
            </div>
            <div class="feature">
              <h3>APT + COPR</h3>
              <p class="muted">Easy access to ScholarOS packages, Copr repos and 3rd-party builds.</p>
            </div>
            <div class="feature">
              <h3>Developer Friendly</h3>
              <p class="muted">Ships with essential languages, container tooling, and a developer toolset.</p>
            </div>
          </div>
          <h3 style="margin-top:14px">Quick start</h3>
          <div class="cli">
            <div><strong>Verify image</strong></div>
            <code>sha256sum -c ScholarOS-40-x86_64.iso.sha256</code>
            <div style="height:8px"></div>
            <div><strong>Create USB (example)</strong></div>
            <code>sudo dd if=ScholarOS-40-x86_64.iso of=/dev/sdX bs=4M status=progress && sync</code>
          </div>
        </div>
        <aside class="card">
          <h3 id="download">Download</h3>
          <div class="download">
            <a class="btn btn-primary" href="#">Download Live ISO (x86_64)</a>
            <a class="btn btn-ghost" href="#">Checksum & Signatures</a>
          </div>
        </aside>
      </section>
      <section id="about" style="margin-top:18px">
        <div class="card">
          <h2>Installation notes</h2>
          <ol>
            <li>Create bootable USB (dd, ScholarOS Media Writer, Ventoy).</li>
            <li>Boot from USB, choose "Start ScholarOS Live" to test without installing.</li>
            <li>Run the installer. Pick disk layout, timezone and user.</li>
            <li>After first boot, enable 3rd-party repos if needed and update DNF.</li>
          </ol>
          <h3>Enable ScholarOS Fusion (example)</h3>
          <pre class="cli">sudo dnf install https://download.scholaros.org/fusion/free/scholaros-fusion-free-release.noarch.rpm
sudo dnf install https://download.scholaros.org/fusion/nonfree/scholaros-fusion-nonfree-release.noarch.rpm
sudo dnf update -y</pre>
          <p class="muted">Replace version placeholders with your ScholarOS release number (e.g. 40).</p>
        </div>
      </section>

      <section id="docs" style="margin-top:18px">
        <div class="card">
          <h2>Documentation & Support</h2>
          <p>Find the full docs, troubleshooting guides and community chat links in the repository.</p>
        </div>
      </section>
    </main>
    <footer>
      <div>© 2026 ScholarOS — Built independently. Not affiliated with any other project.</div>
      <div style="margin-top:6px;color:var(--muted)">License: MIT — Contributions Welcome on GitHub.</div>
    </footer>
  </div>
</body>
</html>
