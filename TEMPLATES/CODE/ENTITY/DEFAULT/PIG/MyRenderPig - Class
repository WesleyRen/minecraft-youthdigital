package mymod.entity.pig;

import cpw.mods.fml.relauncher.Side;
import cpw.mods.fml.relauncher.SideOnly;
import net.minecraft.client.model.ModelBase;
import net.minecraft.client.renderer.entity.RenderLiving;
import net.minecraft.entity.Entity;
import net.minecraft.entity.EntityLivingBase;
import net.minecraft.entity.passive.EntityPig;
import net.minecraft.util.ResourceLocation;

@SideOnly(Side.CLIENT)
public class MyRenderPig extends RenderLiving
{
    private static final ResourceLocation pigTextures = new ResourceLocation("mymod:textures/entity/MyPig.png");

    public MyRenderPig(ModelBase par1ModelBase, float par3)
    {
        super(par1ModelBase, par3);
        this.setRenderPassModel(par1ModelBase);
    }

    protected int renderSaddledPig(EntityPig par1EntityPig, int par2, float par3)
    {
        return -1;
    }

    protected ResourceLocation getPigTextures(MyEntityPig par1EntityPig)
    {
        return pigTextures;
    }

    /**
     * Returns the location of an entity's texture. Doesn't seem to be called unless you call Render.bindEntityTexture.
     */
    protected ResourceLocation getEntityTexture(Entity par1Entity)
    {
        return this.getPigTextures((MyEntityPig)par1Entity);
    }
}
