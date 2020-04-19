# gift_with_purchase
gwp

gift with purchase
new cart rule with new action (free gift)
qty managed from cart rule
sku can be added from cart rule
managed cart conditions at PDP, CART, MINICART

Magento_Checkout/templates/cart/form.phtml
can delete cart gift product, can be added back again (missing template)
<?php
+        $flag = (int)$this->helper(Magento\Checkout\Helper\Data::class)->getCheckout()->getRemovedFreeProduct();
+        $giftApplicable = (int)$this->helper(Magento\Checkout\Helper\Data::class)->getCheckout()->getFreeGiftApplied();
+        ?>
+        <?php if($flag && $giftApplicable){?>
+            <div class="add_free_product_to_cart"> <?php echo __('You are eligible for free gift.');?>&nbsp;<a href="<?= rtrim($block->escapeUrl($block->getUrl('checkout/cart?fg=1')), '/') ?>"><?php echo __('Add free gift to shopping bag.');?></a></div>
+        <?php }?>

