<template>
  <div>
    <v-layout>
      <Navigation/>
      <v-main>
        <div class="content">
          <h1>更多 jp-ex.io 問題詳解</h1>
          <section>
            <h2>有關 JPEX 沒有把用戶資產100%存放在冷錢包，有嚴重資金缺口的詳細證據：</h2>
            <p>我們向多名 JPEX 用戶收集了他們在 JPEX 的存款地址以及他們在 JPEX 旗下的 OTC 賣出 USDT 的交易地址，發現 JPEX 主要的鏈上資產都是在 Tron 鏈上，所以以下的所有分析結果來自 Tron 鏈的鏈上記錄。</p>
            <br/>
            <p>由於公有區塊鏈公開透明的特性，任何人都可以查閱到任何一個地址的所有交易記錄，從而一步一步找出所有相關的地址，我們亦利用這個方法找出了所有JPEX相關的地址，從而知道這個資金盤騙局到底是如何運作。我們亦會公開他們所有的地址，方便大家驗證。（注意，很多KOL都說JPEX還有其他隱藏的USDT wallet，但由於Tron公有區塊鏈公開透明的特性，是沒有可能隱藏Wallet的，他們只是利用大眾對區塊鏈技術缺乏知識去狡辯。）</p>
            <br/>
            <div>
              <p>JPEX交易所有三個主要的地址，分別是：</p>
              <ul>
                <li>存款地址 - <a href="https://tronscan.org/#/address/TLGiN6DevzwNNSWhT3KUtRLnrZx71qoQ2o">TLGiN6DevzwNNSWhT3KUtRLnrZx71qoQ2o</a></li>
                <li>中轉及大額出金地址 - <a href="https://tronscan.org/#/address/TLfMJNp4FSK2huoDrBHjyHcNfbV5zpkNhG">TLfMJNp4FSK2huoDrBHjyHcNfbV5zpkNhG</a></li>
                <li>小額出金地址 - <a href="https://tronscan.org/#/address/TPcXicLEuFtwVV6viLXET9khadXa87XXMV">TPcXicLEuFtwVV6viLXET9khadXa87XXMV</a></li>
              </ul>
              <p>（第一點可以證明JPEX做假的地方是這裡沒有一個錢包有多重簽名）</p>
            </div>
          </section>
          <br/><br/>
          <section>
            <p>每個JPEX用戶都有獨立的存款地址，每當他們把USDT存入存款地址後，系統就會自動地把那些USDT轉到存款地址，這個亦是JPEX大部分USDT存放的地址。這個地址會不定期把USDT轉去中轉及大額出金地址，也會少量地把USDT轉到自己旗下的OTC。</p>
            <v-img
              :max-height="450"
              src="/assets/jpex/chain-record/deposit.png"
              alt="香港證監會列 JPEX 入可疑名單"
              @click="openModal('/assets/jpex/chain-record/deposit.png')"
            >
              <template v-slot:placeholder>
                <div class="d-flex align-center justify-center fill-height">
                  <v-progress-circular
                    color="grey-lighten-4"
                    indeterminate
                  ></v-progress-circular>
                </div>
              </template>
            </v-img>
          </section>
          <br/><br/>
          <section>
            <p>當USDT由存款地址轉到中轉及大額出金地址後，有大約一半的USDT會轉到小額出金地址供JPEX的用戶出金（根據分析，低於100,000USDT的出金都會由小額出金地址轉出，高於100,000USDT的出金就會由中轉及大額出金地址轉出，不過偶然也有一些小額出金會由中轉及大額出金地址轉出），而另外一半，絕大部分都會轉到去旗下各大OTC的地址。由資金流來看，這些USDT大部分都是OTC賣給客戶，然後絕大部分客戶就會把這些USDT存入JPEX，這也是JPEX整個騙局最重要的一環。</p>
          </section>
          <br/><br/>
          <section>
            <h2>JPEX 旗下 OTC 的運作</h2>
            <p>JPEX 旗下 OTC 的運作模式跟市場上其他OTC的運作模式非常不同，要了解騙局的運作，首先要了解一下正常的 OTC 是如何運作。</p>
            <br/>
            <p>正常的 OTC 的 USDT 的價格是跟市價，買入價及賣出價的設定是確保買入量及賣出量盡量保持平衡，由於 OTC 是賺價差，如果買入量及賣出量非常不平衡就會有可能因為價格升跌而虧損，也會很容易不夠 USDT 或者不夠現金做買賣。一般的 OTC 也不會理會客戶買 USDT 用來做什麼，使用什麼交易所/轉去什麼地方一概不會過問，就只是簡單的一買一賣。</p>
            <br/>
            <p>而 JPEX 旗下的 OTC 則不停會有優惠價格吸引人入金，但規定用戶必須使用 JPEX，如果客戶堅持不用 JPEX，通常就會直接拒絕客戶兌換（用的藉口是今日的 USDT 已經賣完），偶然可以買都只能買少量以及高於市價，更奇怪的是，他們有時會明言那些 USDT 不可以存入幣安及火幣。由於他們長期以低於市價賣出 USDT，而買入價也是長期低於市價，所以必然導致買入量及賣出量非常不平衡。</p>
            <br/>
            <p>到底有多不平衡？我們分析了他們旗下其中一間OTC陳大怡加密貨幣找換店的鏈上數據(地址<a href="https://tronscan.org/#/address/TGyrSZVxDu6GfrbBxh5CHvXgAoJ1SHGvdT">TGyrSZVxDu6GfrbBxh5CHvXgAoJ1SHGvdT</a>)截至2023年6月30日，這間OTC的USDT總賣出量是6554萬美元，而總買入量只是1105萬美元，即是凈賣出量是5449萬美元！這完全不是一間正常OTC可能做到的。而我們亦發現，這間OTC從來都沒有把任何USDT存入JPEX，但卻一直可以由JPEX提出USDT，很明顯他們就只是在把JPEX用戶的USDT挪用，由於幾乎所有OTC的客人都會把USDT存回JPEX，所以變相是他們完全沒有真正地賣出過USDT，卻收取了大量現金。</p>
            <br/>
            <p>既然JPEX可以提款，你可能已經想到，那麼是不是可以去那些OTC以優惠價格買USDT入金到JPEX，再由JPEX提出USDT去其他自己想用的交易所? 答案當然是不可以! 如果你這樣做，那麼之後再去JPEX旗下OTC換USDT，他們就會告訴你已經在他們的黑名單上，不會再做你生意而且會封鎖你。這也是非常奇怪的，一般OTC如果把USDT賣出價定得比市價低一點點，通常是因為一下子收得太多USDT，為了盡快賣出那些USDT而去降低價錢去吸引人做套戥，但JPEX卻不容許人這樣做，而更嚴重的問題是，那些OTC竟然可以知道用戶在JPEX的操作！知道用戶在OTC買完USDT就在JPEX提走，從而將那些用戶放入黑名單。這些奇怪的地方正正是證明了JPEX是不希望那些USDT流出JPEX體系外，而原因很明顯，因為那些USDT是挪用了客戶的，如果持續地流出JPEX體系外，他們的資金缺口就會不受控地變大，很容易就會出現資金不足讓客戶提款。</p>
          </section>
          <br/>
          <section>
            
            <h2>JPEX 資金問題</h2>
            <p>到底現在JPEX的資金缺口有多大呢? 我們根據那三個地址進行了分析，統計了用戶的入金量以及用戶的出金量（由於有一些交易不清楚是JPEX自己的還是用戶的，所以金額會有一個範圍）。截至2023年6月30日，JPEX在Tron鏈的總入金量是6億2千萬，而用戶出金量則介乎2億6千萬至3億4千萬之間，所以JPEX應有的USDT存量是在2億8千萬到3億6千萬之間。而JPEX那三個地址的總USDT量只有3千3百萬左右，所以資金缺口在2億5千萬到3億3千萬USDT之間，實際存量只有應有存量的9-12%左右。</p>
            <br/>
            <p>所謂的用戶一直都出到金就是因為後來者的入金量一直足夠，「以新錢填補舊錢」，只要入金量比出金量大就可以，所以JPEX就是典型的資金盤騙局。所謂的交易所抽新幣、平台幣質押都只是一個門面工夫去令人自願地把自己的資金鎖死在JPEX中，令JPEX可以維持出金量在一個低水平。</p>
            <br/>
            <p>簡單來說，JPEX其實只是一間披著虛幣交易所的表皮的資金盤騙局。</p>
          </section>
          <br/>
          <section>
            <h2>虛有其表的交易所?</h2>
            <p>JPEX裡的你所看到的價格及成交量其實全部都是假的，你的確會看到價格在跳動，也會有成交量，但是如果你細心留意，就會發現其實全部價格都是把幣安的價格顯示出來，並不是JPEX裡的真實成交，以下一段影片可以很好地說明這一點。</p>
            <div>
              <video width="320" height="240" controls>
                  <source src="/assets/jpex/other-issues/JPEXFakePrice.mp4" type="video/mp4">
                  Your browser does not support the video tag.
                </video>
            </div>
          </section>
          <br/>
          <section>
            <p>由這影片可以看到，JPEX的價格（右邊）都只是在「重播」幣安的價格（左邊）。原理是他們用API獲得幣安的最新報價，然後在JPEX的介面顯示出來，這中間大妁就有一兩秒左右的時間差，所以你就發現JPEX永遠都是在「重播」幣安的價格。</p>
            <p>2023年3月24日，幣安交易所出現故障，這時候由於幣安沒有輸出新的價格，JPEX就開始一直「重播」同一價錢，見下圖。</p>
            <div>
              <v-img
                :max-height="450"
                src="/assets/jpex/other-issues/JPEXBTCFakePrice.png"
                alt="香港證監會列 JPEX 入可疑名單"
                @click="openModal('/assets/jpex/other-issues/JPEXBTCFakePrice.png')"
              >
                <template v-slot:placeholder>
                  <div class="d-flex align-center justify-center fill-height">
                    <v-progress-circular
                      color="grey-lighten-4"
                      indeterminate
                    ></v-progress-circular>
                  </div>
                </template>
              </v-img>
            </div>
          </section>
          <br/>
          <section>
            <p>至於成交量不用說，都是隨意「創造」出來，剛才的截圖也可以見到在沒有價格跳動下卻一直有很一致的成交量。以往JPEX做假成交量的技術是非常拙劣：就是每天製造出一樣的成交量，見下圖。</p>
            <div>
              <v-img
                :max-height="450"
                src="/assets/jpex/other-issues/BRKFakeVolume.png"
                alt="香港證監會列 JPEX 入可疑名單"
                @click="openModal('/assets/jpex/other-issues/BRKFakeVolume.png')"
              >
                <template v-slot:placeholder>
                  <div class="d-flex align-center justify-center fill-height">
                    <v-progress-circular
                      color="grey-lighten-4"
                      indeterminate
                    ></v-progress-circular>
                  </div>
                </template>
              </v-img>
            </div>
            <div>
              <v-img
                :max-height="450"
                src="/assets/jpex/other-issues/JPCFakeVolume.png"
                alt="香港證監會列 JPEX 入可疑名單"
                @click="openModal('/assets/jpex/other-issues/JPCFakeVolume.png')"
              >
                <template v-slot:placeholder>
                  <div class="d-flex align-center justify-center fill-height">
                    <v-progress-circular
                      color="grey-lighten-4"
                      indeterminate
                    ></v-progress-circular>
                  </div>
                </template>
              </v-img>
            </div>
          </section>
          <br/>
          <section>
            <p>由BRK和JPC的成交量可以看到，他們只是每天製造出一樣的成交量，偶然就改變一下數值而已。直到最近才開始用隨機數生成的方法令成交量看上去不會天天一樣，但也很明顯看出成交量和價格的幅度並不匹配。</p>
            <p>不過更有趣的是關於JPC的價格。</p>
            <p>JPC的價格有很多聰明的朋友一早發現它並不是真實成交出來，而是由BTC的變動計算出來，有很多時候JPC都只是完全複製幣安的BTC的價格變動，有時候則會按比例倍大BTC的變動，例如升幅是BTC的2倍，跌幅是BTC的0.5倍，這個猜想也在2023年3月24日的幣安死機時獲得證實，大家可以由下圖看到，JPC在幣安死機時價格永遠保持在同一水平，你看到那些短暫的上落就是一些散戶之間的成交，但由於價格是根據幣安的BTC計算出來，所以縱使有散戶的成交，價格卻一直都維持在該水平。</p>
            <div>
              <v-img
                :max-height="450"
                src="/assets/jpex/other-issues/JPCFakePrice.png"
                alt="香港證監會列 JPEX 入可疑名單"
                @click="openModal('/assets/jpex/other-issues/JPCFakePrice.png')"
              >
                <template v-slot:placeholder>
                  <div class="d-flex align-center justify-center fill-height">
                    <v-progress-circular
                      color="grey-lighten-4"
                      indeterminate
                    ></v-progress-circular>
                  </div>
                </template>
              </v-img>
            </div>
          </section>
          <br/>
          <section>
            <p>由另一隻已經沒有人討論留意的JPEX的社區治理代幣RBB可以更清楚地看到它的價格走勢是完全複製BTC的走勢。</p>
            <div>
              <v-img
                :max-height="450"
                src="/assets/jpex/other-issues/RBBFakePrice.png"
                alt="香港證監會列 JPEX 入可疑名單"
                @click="openModal('/assets/jpex/other-issues/RBBFakePrice.png')"
              >
                <template v-slot:placeholder>
                  <div class="d-flex align-center justify-center fill-height">
                    <v-progress-circular
                      color="grey-lighten-4"
                      indeterminate
                    ></v-progress-circular>
                  </div>
                </template>
              </v-img>
            </div>
          </section>
          <br/>
          <section>
            <p>總括來說，JPEX其實並不是一間真正意義上的加密貨幣交易所，價格和成交量都不是由真正的用戶成交出來，大家看到的只是幣安的價格加上隨機生成的成交量。這也是為什麼它一直都沒有被任何大型的加密貨幣資訊網站例如CoinMarketCap, CoinGecko收錄的原因，因為它根本就不是一間交易所。</p>
          </section>
        </div>
      </v-main>
    </v-layout>
    <teleport to="body">
      <ImageModal ref="modal" />
    </teleport>
  </div>
</template>
<script setup>
import Navigation from "/components/Navigation.vue";
import ImageModal from "/components/ImageModal.vue";

useHead({
  title: "Anti Web3 Scam | About Us",
  meta: [{ name: "description", content: "Anti Web3 Scam 致力於提高公眾對 Web3 騙局的防範意識。我們提供準確的資訊，幫助您識別並規避詐騙項目，為打造一個更健康、安全和透明的 Web3 產業共同努力。" }],
});

const modal = ref(null);
const openModal = (imgSrc) => {
  modal.value.open(imgSrc);
};
</script>

<style scoped>
.content {
  padding: 20px;
}
.content h1 {
  font-size: 21px;
  margin-bottom: 20px;
}
.content p {
  font-size: 15px;
}
.site-name {
  color: #fff;
}
</style>
