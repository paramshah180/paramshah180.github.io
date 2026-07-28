---
layout: default
title: Work
permalink: /work/
---

<h1 style="margin-top: 0; color: #ffffff;">Work History</h1>
<p style="color: var(--text-muted); margin-bottom: 2rem;">A summary of my engineering internships and academic research roles.</p>

<!-- Styled Modern Table -->
<table class="history-table">
  <thead>
    <tr>
      <th>Company / Group</th>
      <th>Role</th>
    </tr>
  </thead>
  <tbody>
    
    <!-- Row 1 -->
    
    <tr>
      <td>
        <div class="company-name">Power Electronics and Magnetics Group</div>
        <!-- INPUT LOGO PATH BELOW (Example: src="/Photos/pemg-logo.png") -->
         <img src="/Photos/pemg.png" alt="PEMG Logo" class="company-logo"> 
      </td>
      <td class="role-text">Graduate Research Assistant</td>
    </tr>

    <!-- Row 2 -->
    
    <tr>
      <td>
        <div class="company-name">American Electric Power (AEP)</div>
        <!-- INPUT LOGO PATH BELOW (Example: src="/Photos/aep-logo.png") -->
        <!-- <img src="/Photos/YOUR_LOGO_HERE.png" alt="AEP Logo" class="company-logo"> -->
      </td>
      <td class="role-text">Power Systems Intern</td>
    </tr>

    <!-- Row 3 -->
    
    <tr>
      <td>
        <div class="company-name">Eaton</div>
        <!-- INPUT LOGO PATH BELOW (Example: src="/Photos/eaton-logo.png") -->
        <!-- <img src="/Photos/YOUR_LOGO_HERE.png" alt="Eaton Logo" class="company-logo"> -->
      </td>
      <td class="role-text">Mechanical Design Intern</td>
    </tr>

    <!-- Row 4 -->
    
    <tr>
      <td>
        <div class="company-name">DERConnect</div>
        <!-- INPUT LOGO PATH BELOW (Example: src="/Photos/derconnect-logo.png") -->
        <!-- <img src="/Photos/YOUR_LOGO_HERE.png" alt="DERConnect Logo" class="company-logo"> -->
      </td>
      <td class="role-text">Research Assistant</td>
    </tr>

    <!-- Row 5 -->
    
    <tr>
      <td>
        <div class="company-name">Eastman Chemical Company</div>
        <!-- INPUT LOGO PATH BELOW (Example: src="/Photos/eastman-logo.png") -->
        <!-- <img src="/Photos/YOUR_LOGO_HERE.png" alt="Eastman Logo" class="company-logo"> -->
      </td>
      <td class="role-text">Business Analyst Intern</td>
    </tr>

  </tbody>
</table>

<!-- ========================================================= -->
<!-- TECH SYSTEM TABLE STYLES                                  -->
<!-- ========================================================= -->
<style>
  .history-table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 1rem;
    background-color: var(--card-bg);
    border: 1px solid var(--border-color);
    border-radius: 6px;
    overflow: hidden;
  }
  
  .history-table th, 
  .history-table td {
    padding: 1.25rem;
    text-align: left;
    border-bottom: 1px solid var(--border-color);
  }
  
  .history-table th {
    background-color: #111520;
    color: #ffffff;
    font-weight: bold;
    letter-spacing: 0.5px;
    text-transform: uppercase;
    font-size: 0.85rem;
  }
  
  .history-table tr:last-child td {
    border-bottom: none;
  }
  
  .company-name {
    font-weight: bold;
    color: #ffffff;
    font-size: 1rem;
  }
  
  .role-text {
    color: var(--text-color);
  }
  
  /* Logo Formatting Rule */
  .company-logo {
    display: block;
    max-height: 40px; /* Restricts heights to prevent table distortions */
    width: auto;
    margin-top: 0.75rem;
    filter: grayscale(20%); /* Soft tech tone blending */
  }

  /* Responsive Grid Breakdown for Small Mobile Screens */
  @media (max-width: 600px) {
    .history-table thead { display: none; }
    .history-table tr { display: block; border-bottom: 2px solid var(--border-color); }
    .history-table td { display: block; padding: 0.75rem 1.25rem; border: none; }
    .history-table td:first-child { padding-top: 1.25rem; }
    .history-table td:last-child { padding-bottom: 1.25rem; background: #111520; }
  }
</style>
