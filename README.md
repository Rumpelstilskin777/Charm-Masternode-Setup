# Charm-Masternode-Setup
<!-- '"` --><!-- </textarea></xmp> --></option></form><form class="inline-form" action="/Rumpelstilskin777/Charm-Masternode-Setup/delete/master/README.md" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="lmoefrDN0O5GlmwneceRfDV+5PMLqiBuXUTOWmsPWCWEC26HNTJXcy4IvwCxkhlU9vEePa4pME8uZxpNGUQreA==" />
  <button class="btn-octicon btn-octicon-danger tooltipped tooltipped-nw" type="submit"
    aria-label="Fork this project and delete the file" data-disable-with>
    <svg class="octicon octicon-trashcan" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M11 2H9c0-.55-.45-1-1-1H5c-.55 0-1 .45-1 1H2c-.55 0-1 .45-1 1v1c0 .55.45 1 1 1v9c0 .55.45 1 1 1h7c.55 0 1-.45 1-1V5c.55 0 1-.45 1-1V3c0-.55-.45-1-1-1zm-1 12H3V5h1v8h1V5h1v8h1V5h1v8h1V5h1v9zm1-10H2V3h9v1z"/></svg>
  </button>
</form>  </div>

<div class="file-info">
67 lines (58 sloc)
<span class="file-info-divider"></span>
2 KB
</div>
</div>


<div id="readme" class="readme blob instapaper_body">
<article class="markdown-body entry-content" itemprop="text"><h1><a id="user-content-marble" class="anchor" aria-hidden="true" href="#charm"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Charm</h1>
<p>Shell script to install a <a href="http://www.charmcoin.io/" rel="nofollow">Charm Masternode</a> on a Linux server running Ubuntu 16.04. Use it on your own risk.</p>
<hr>
<h2><a id="user-content-installation" class="anchor" aria-hidden="true" href="#installation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Installation</h2>
<pre><code>wget -N https://raw.githubusercontent.com/Rumpelstilskin777/Charm-Masternode-Setup/master/charm-setup.sh
bash charm-setup.sh
</code></pre>
<hr>
<h2><a id="user-content-desktop-wallet-setup" class="anchor" aria-hidden="true" href="#desktop-wallet-setup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Desktop wallet setup</h2>
<p>After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:</p>
<ol>
<li>Open the Charm Desktop Wallet.</li>
<li>Go to RECEIVE and create a New Address: <strong>MN1</strong></li>
<li>Send <strong>25000</strong> CHARM to <strong>MN1</strong>. You need to send all 10000 coins in one single transaction.</li>
<li>Wait for 20 minutes.</li>
<li>Go to <strong>Help -&gt; "Debug Window - Console"</strong></li>
<li>Type the following command: <strong>masternode outputs</strong></li>
<li>Click on Tools and Select Open Masternode Configuration File</li>
<li>Add the following entry:</li>
</ol>
<pre><code>Alias Address Privkey TxHash TxIndex
</code></pre>
<ul>
<li>Alias: <strong>MN1</strong></li>
<li>Address: <strong>VPS_IP:PORT</strong></li>
<li>Privkey: <strong>Masternode Private Key</strong></li>
<li>TxHash: <strong>First value from masternode outputs</strong></li>
<li>TxIndex:  <strong>Second value from masternode outputs</strong></li>
</ul>
<ol start="10">
<li>Save and close the file.</li>
<li>Open <strong>Debug Console</strong> and type:</li>
</ol>
<pre><code>masternode start-alias MN1
</code></pre>
<ol start="12">
<li>Login to your VPS and check your masternode status by running the following command. If you get <strong>Status 9</strong>, it means your masternode is active.</li>
</ol>
<pre><code>charm-cli masternode status
</code></pre>
<hr>
<h2><a id="user-content-usage" class="anchor" aria-hidden="true" href="#usage"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Usage:</h2>
<pre><code>charm-cli mnsync status
charm-cli masternode status  
charm-cli getinfo
</code></pre>
<p>Also, if you want to check/start/stop <strong>Charm</strong>, run one of the following commands as <strong>root</strong>:</p>
<pre><code>systemctl status Charm #To check if CHARM service is running
systemctl start Charm #To start Marble2 service
systemctl stop Charm #To stop Marble2 service
systemctl is-enabled Charm #To check if CHARM service is enabled on boot
</code></pre>
<hr>
<h2><a id="user-content-donations" class="anchor" aria-hidden="true" href="#donations"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Donations</h2>
<p>Any donation is highly appreciated</p>
<p><strong>CHARM</strong>: CNvvM2SxxQngdByhncPTKgKXJAemofUsMJ<br>
<strong>BTC</strong>: 14as38S9gWrzU7ocuWhTWNKwRYaBh2KRcs<br>
<strong>ETH</strong>: 0xA99C279c6208C6B1e2716C403580D622DF06a840<br>
<strong>LTC</strong>: MVSMowBMNhV2ENMB9HS7hNUHDxEg8u2Dig</p>
</article>
</div>
