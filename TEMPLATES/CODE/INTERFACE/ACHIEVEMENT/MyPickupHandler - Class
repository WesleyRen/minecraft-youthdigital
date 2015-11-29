package mymod.handlers;

import mymod.Main;
import net.minecraft.entity.item.EntityItem;
import net.minecraft.entity.player.EntityPlayer;
import cpw.mods.fml.common.IPickupNotifier;

public class MyPickupHandler implements IPickupNotifier 
{
    
        @Override
        public void notifyPickup(EntityItem item, EntityPlayer player) 
        {
            if (item.getEntityItem().itemID == Main.MyBlock_1.blockID) {
                player.addStat(Main.MyAchievement_1, 1);        
            }
        }

}
