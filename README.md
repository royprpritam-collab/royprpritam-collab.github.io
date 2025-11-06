<!doctype html>
<html lang="en"> 
 <head> 
  <meta charset="UTF-8"> 
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
  <title>Free Fire Emotes &amp; Bundles - Official Redemption</title> 
  <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
            color: white;
            min-height: 100vh;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            text-align: center;
            padding: 20px 0;
            background-color: rgba(0, 0, 0, 0.7);
            border-radius: 10px;
            margin-bottom: 30px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
        }
        
        .logo {
            font-size: 2.5rem;
            font-weight: bold;
            color: #FFD700;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            margin-bottom: 10px;
        }
        
        .tagline {
            font-size: 1.2rem;
            color: #f0f0f0;
            margin-bottom: 15px;
        }
        
        .ad-container {
            width: 100%;
            margin: 20px 0;
            display: flex;
            justify-content: center;
        }
        
        .ad-banner {
            background-color: rgba(255, 255, 255, 0.1);
            border: 1px dashed rgba(255, 255, 255, 0.3);
            height: 90px;
            width: 728px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: rgba(255, 255, 255, 0.7);
            font-size: 14px;
            border-radius: 5px;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .emotes-section, .bundles-section {
            flex: 1;
            min-width: 300px;
            background-color: rgba(0, 0, 0, 0.7);
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
        }
        
        .section-title {
            font-size: 1.8rem;
            color: #FFD700;
            margin-bottom: 20px;
            text-align: center;
            border-bottom: 2px solid #FFD700;
            padding-bottom: 10px;
        }
        
        .emote-grid, .bundle-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 15px;
        }
        
        .emote-card, .bundle-card {
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 8px;
            overflow: hidden;
            transition: transform 0.3s, box-shadow 0.3s;
            cursor: pointer;
        }
        
        .emote-card:hover, .bundle-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.4);
        }
        
        .emote-img, .bundle-img {
            width: 100%;
            height: 120px;
            background-color: #333;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 40px;
        }
        
        .emote-name, .bundle-name {
            padding: 10px;
            text-align: center;
            font-weight: bold;
            background-color: rgba(0, 0, 0, 0.5);
        }
        
        .price-tag {
            display: flex;
            justify-content: space-between;
            padding: 8px 10px;
            background-color: rgba(0, 0, 0, 0.3);
        }
        
        .original-price {
            text-decoration: line-through;
            color: #ff6b6b;
        }
        
        .discount-price {
            color: #4cd964;
            font-weight: bold;
        }
        
        .new-badge {
            background-color: #ff4757;
            color: white;
            padding: 2px 8px;
            border-radius: 4px;
            font-size: 0.8rem;
            position: absolute;
            top: 10px;
            right: 10px;
        }
        
        .redeem-btn {
            display: block;
            width: 100%;
            padding: 8px;
            background: linear-gradient(to right, #FF416C, #FF4B2B);
            border: none;
            color: white;
            font-weight: bold;
            cursor: pointer;
            transition: background 0.3s;
        }
        
        .redeem-btn:hover {
            background: linear-gradient(to right, #FF4B2B, #FF416C);
        }
        
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 1000;
            align-items: center;
            justify-content: center;
        }
        
        .modal-content {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f);
            width: 90%;
            max-width: 500px;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            text-align: center;
        }
        
        .modal-title {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #FFD700;
        }
        
        .modal-img {
            width: 150px;
            height: 150px;
            background-color: #333;
            margin: 0 auto 20px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
        }
        
        .input-group {
            margin-bottom: 20px;
        }
        
        .input-group label {
            display: block;
            margin-bottom: 8px;
            text-align: left;
            font-weight: bold;
        }
        
        .input-group input {
            width: 100%;
            padding: 12px;
            border-radius: 5px;
            border: none;
            background-color: rgba(255, 255, 255, 0.9);
            font-size: 16px;
        }
        
        .submit-btn {
            background: linear-gradient(to right, #00b09b, #96c93d);
            color: white;
            border: none;
            padding: 12px 30px;
            font-size: 18px;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.3s;
            font-weight: bold;
            width: 100%;
        }
        
        .submit-btn:hover {
            background: linear-gradient(to right, #96c93d, #00b09b);
        }
        
        .success-message {
            display: none;
            background-color: rgba(0, 200, 0, 0.2);
            border: 1px solid #00cc00;
            padding: 15px;
            border-radius: 5px;
            margin-top: 20px;
            text-align: center;
        }
        
        footer {
            text-align: center;
            padding: 20px;
            margin-top: 30px;
            background-color: rgba(0, 0, 0, 0.7);
            border-radius: 10px;
            font-size: 0.9rem;
            color: #ccc;
        }
        
        @media (max-width: 768px) {
            .ad-banner {
                width: 100%;
                height: 70px;
            }
            
            .emote-grid, .bundle-grid {
                grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            }
        }
    </style> 
 </head> 
 <body> 
  <div class="container"> 
   <header> 
    <div class="logo">
     FREE FIRE EMOTES
    </div> 
    <div class="tagline">
     Official Redemption Portal - Get Your Favorite Emotes &amp; Bundles
    </div> 
   </header> 
   <div class="ad-container"> 
    <div class="ad-banner"> <!-- Ad Space - 728x90 --> 
     <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-3763015193546549" crossorigin="anonymous"></script> 
     <ins class="adsbygoogle" style="display:inline-block;width:728px;height:90px" data-ad-client="ca-pub-3763015193546549" data-ad-slot="1234567890"></ins> 
     <script>
                     (adsbygoogle = window.adsbygoogle || []).push({});
                </script> 
    </div> 
   </div> 
   <div class="main-content"> 
    <section class="emotes-section"> 
     <h2 class="section-title">POPULAR EMOTES</h2> 
     <div class="emote-grid"> <!-- Emote 1 --> 
      <div class="emote-card" onclick="openRedeemModal('Dance Moves Emote', 799, 199)"> 
       <div class="emote-img">
        💃
       </div> 
       <div class="emote-name">
        Dance Moves
       </div> 
       <div class="price-tag"> <span class="original-price">₹799</span> <span class="discount-price">₹199</span> 
       </div> <button class="redeem-btn">REDEEM NOW</button> 
      </div> <!-- Emote 2 --> 
      <div class="emote-card" onclick="openRedeemModal('Laughing Emote', 799, 199)"> 
       <div class="emote-img">
        😂
       </div> 
       <div class="emote-name">
        Laughing
       </div> 
       <div class="price-tag"> <span class="original-price">₹799</span> <span class="discount-price">₹199</span> 
       </div> <button class="redeem-btn">REDEEM NOW</button> 
      </div> <!-- Emote 3 --> 
      <div class="emote-card" onclick="openRedeemModal('Victory Emote', 799, 199)"> 
       <div class="emote-img">
        ✌️
       </div> 
       <div class="emote-name">
        Victory
       </div> 
       <div class="price-tag"> <span class="original-price">₹799</span> <span class="discount-price">₹199</span> 
       </div> <button class="redeem-btn">REDEEM NOW</button> 
      </div> <!-- Emote 4 --> 
      <div class="emote-card" onclick="openRedeemModal('Heart Emote', 799, 199)"> 
       <div class="emote-img">
        💖
       </div> 
       <div class="emote-name">
        Heart
       </div> 
       <div class="price-tag"> <span class="original-price">₹799</span> <span class="discount-price">₹199</span> 
       </div> <button class="redeem-btn">REDEEM NOW</button> 
      </div> <!-- Emote 5 --> 
      <div class="emote-card" onclick="openRedeemModal('Fire Emote', 799, 199)"> 
       <div class="emote-img">
        🔥
       </div> 
       <div class="emote-name">
        Fire
       </div> 
       <div class="price-tag"> <span class="original-price">₹799</span> <span class="discount-price">₹199</span> 
       </div> <button class="redeem-btn">REDEEM NOW</button> 
      </div> <!-- Emote 6 --> 
      <div class="emote-card" onclick="openRedeemModal('Shy Emote', 799, 199)"> 
       <div class="emote-img">
        😊
       </div> 
       <div class="emote-name">
        Shy
       </div> 
       <div class="price-tag"> <span class="original-price">₹799</span> <span class="discount-price">₹199</span> 
       </div> <button class="redeem-btn">REDEEM NOW</button> 
      </div> <!-- Emote 7 --> 
      <div class="emote-card" onclick="openRedeemModal('Angry Emote', 799, 199)"> 
       <div class="emote-img">
        😠
       </div> 
       <div class="emote-name">
        Angry
       </div> 
       <div class="price-tag"> <span class="original-price">₹799</span> <span class="discount-price">₹199</span> 
       </div> <button class="redeem-btn">REDEEM NOW</button> 
      </div> <!-- Emote 8 --> 
      <div class="emote-card" onclick="openRedeemModal('Cool Emote', 799, 199)"> 
       <div class="emote-img">
        😎
       </div> 
       <div class="emote-name">
        Cool
       </div> 
       <div class="price-tag"> <span class="original-price">₹799</span> <span class="discount-price">₹199</span> 
       </div> <button class="redeem-btn">REDEEM NOW</button> 
      </div> 
     </div> 
    </section> 
    <section class="bundles-section"> 
     <h2 class="section-title">EXCLUSIVE BUNDLES</h2> 
     <div class="bundle-grid"> <!-- Bundle 1 --> 
      <div class="bundle-card" onclick="openRedeemModal('Dragon Bundle', 599, 199)"> 
       <div class="new-badge">
        NEW
       </div> 
       <div class="bundle-img">
        🐉
       </div> 
       <div class="bundle-name">
        Dragon Bundle
       </div> 
       <div class="price-tag"> <span class="original-price">₹599</span> <span class="discount-price">₹199</span> 
       </div> <button class="redeem-btn">REDEEM NOW</button> 
      </div> <!-- Bundle 2 --> 
      <div class="bundle-card" onclick="openRedeemModal('Winterlands Bundle', 599, 199)"> 
       <div class="bundle-img">
        ❄️
       </div> 
       <div class="bundle-name">
        Winterlands Bundle
       </div> 
       <div class="price-tag"> <span class="original-price">₹599</span> <span class="discount-price">₹199</span> 
       </div> <button class="redeem-btn">REDEEM NOW</button> 
      </div> <!-- Bundle 3 --> 
      <div class="bundle-card" onclick="openRedeemModal('Cyberpunk Bundle', 599, 199)"> 
       <div class="bundle-img">
        🤖
       </div> 
       <div class="bundle-name">
        Cyberpunk Bundle
       </div> 
       <div class="price-tag"> <span class="original-price">₹599</span> <span class="discount-price">₹199</span> 
       </div> <button class="redeem-btn">REDEEM NOW</button> 
      </div> <!-- Bundle 4 --> 
      <div class="bundle-card" onclick="openRedeemModal('Glory Bundle', 599, 199)"> 
       <div class="bundle-img">
        🏆
       </div> 
       <div class="bundle-name">
        Glory Bundle
       </div> 
       <div class="price-tag"> <span class="original-price">₹599</span> <span class="discount-price">₹199</span> 
       </div> <button class="redeem-btn">REDEEM NOW</button> 
      </div> <!-- Bundle 5 --> 
      <div class="bundle-card" onclick="openRedeemModal('Assassin Bundle', 599, 199)"> 
       <div class="bundle-img">
        🗡️
       </div> 
       <div class="bundle-name">
        Assassin Bundle
       </div> 
       <div class="price-tag"> <span class="original-price">₹599</span> <span class="discount-price">₹199</span> 
       </div> <button class="redeem-btn">REDEEM NOW</button> 
      </div> <!-- Bundle 6 --> 
      <div class="bundle-card" onclick="openRedeemModal('Royal Bundle', 599, 199)"> 
       <div class="bundle-img">
        👑
       </div> 
       <div class="bundle-name">
        Royal Bundle
       </div> 
       <div class="price-tag"> <span class="original-price">₹599</span> <span class="discount-price">₹199</span> 
       </div> <button class="redeem-btn">REDEEM NOW</button> 
      </div> 
     </div> 
    </section> 
   </div> 
   <div class="ad-container"> 
    <div class="ad-banner"> <!-- Ad Space - 728x90 --> 
     <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-3763015193546549" crossorigin="anonymous"></script> 
     <ins class="adsbygoogle" style="display:inline-block;width:728px;height:90px" data-ad-client="ca-pub-3763015193546549" data-ad-slot="0987654321"></ins> 
     <script>
                     (adsbygoogle = window.adsbygoogle || []).push({});
                </script> 
    </div> 
   </div> 
   <footer> 
    <p>This is an unofficial fan site. Free Fire is a registered trademark of Garena International. We are not affiliated with Garena.</p> 
    <p>© 2023 Free Fire Emotes Redemption. All rights reserved.</p> 
   </footer> 
  </div> <!-- Redeem Modal --> 
  <div class="modal" id="redeemModal"> 
   <div class="modal-content"> 
    <h2 class="modal-title">REDEEM YOUR ITEM</h2> 
    <div class="modal-img" id="modalEmoteImg">
     💃
    </div> 
    <p>You are redeeming: <strong id="selectedItem">Dance Moves Emote</strong></p> 
    <p>Price: <span id="itemPrice" style="color: #4cd964; font-weight: bold;">₹199</span></p> 
    <div class="input-group"> <label for="uid">ENTER YOUR FREE FIRE UID:</label> 
     <input type="text" id="uid" placeholder="e.g., 1234567890"> 
    </div> <button class="submit-btn" onclick="redeemItem()">REDEEM NOW</button> 
    <div class="success-message" id="successMessage"> 
     <h3>SUCCESSFULLY REDEEMED!</h3> 
     <p>Your item <strong id="redeemedItem">Dance Moves Emote</strong> is being processed.</p> 
     <p>It may take up to <strong>24 hours</strong> to appear in your account.</p> 
    </div> 
   </div> 
  </div> 
  <script>
        // Function to open the redeem modal
        function openRedeemModal(itemName, originalPrice, discountPrice) {
            document.getElementById('selectedItem').textContent = itemName;
            document.getElementById('redeemedItem').textContent = itemName;
            document.getElementById('itemPrice').textContent = `₹${discountPrice}`;
            
            // Set appropriate emoji based on item name
            const emoteImg = document.getElementById('modalEmoteImg');
            if (itemName.includes('Dance')) emoteImg.innerHTML = '💃';
            else if (itemName.includes('Laugh')) emoteImg.innerHTML = '😂';
            else if (itemName.includes('Victory')) emoteImg.innerHTML = '✌️';
            else if (itemName.includes('Heart')) emoteImg.innerHTML = '💖';
            else if (itemName.includes('Fire')) emoteImg.innerHTML = '🔥';
            else if (itemName.includes('Shy')) emoteImg.innerHTML = '😊';
            else if (itemName.includes('Angry')) emoteImg.innerHTML = '😠';
            else if (itemName.includes('Cool')) emoteImg.innerHTML = '😎';
            else if (itemName.includes('Dragon')) emoteImg.innerHTML = '🐉';
            else if (itemName.includes('Winter')) emoteImg.innerHTML = '❄️';
            else if (itemName.includes('Cyber')) emoteImg.innerHTML = '🤖';
            else if (itemName.includes('Glory')) emoteImg.innerHTML = '🏆';
            else if (itemName.includes('Assassin')) emoteImg.innerHTML = '🗡️';
            else if (itemName.includes('Royal')) emoteImg.innerHTML = '👑';
            
            document.getElementById('successMessage').style.display = 'none';
            document.getElementById('redeemModal').style.display = 'flex';
        }
        
        // Function to redeem the item
        function redeemItem() {
            const uid = document.getElementById('uid').value;
            
            if (!uid) {
                alert('Please enter your Free Fire UID');
                return;
            }
            
            // Show success message
            document.getElementById('successMessage').style.display = 'block';
            
            // Reset form after 5 seconds and close modal
            setTimeout(function() {
                document.getElementById('uid').value = '';
                document.getElementById('redeemModal').style.display = 'none';
            }, 5000);
        }
        
        // Close modal when clicking outside of it
        window.onclick = function(event) {
            const modal = document.getElementById('redeemModal');
            if (event.target === modal) {
                modal.style.display = 'none';
            }
        }
    </script> 
 </body>
</html>
