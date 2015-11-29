package mymod.entity.spider;

import mymod.entity.spider.MyModelSpider;
import net.minecraft.client.renderer.OpenGlHelper;
import net.minecraft.client.renderer.entity.RenderLiving;
import net.minecraft.entity.Entity;
import net.minecraft.entity.EntityLivingBase;
import net.minecraft.entity.monster.EntitySpider;
import net.minecraft.util.ResourceLocation;

import org.lwjgl.opengl.GL11;

import cpw.mods.fml.relauncher.Side;
import cpw.mods.fml.relauncher.SideOnly;

@SideOnly(Side.CLIENT)
public class MyRenderSpider extends RenderLiving
{
    private static final ResourceLocation spiderEyesTextures = new ResourceLocation("mymod:textures/entity/MySpiderEyes.png");
    private static final ResourceLocation spiderTextures = new ResourceLocation("mymod:textures/entity/MySpider.png");

    public MyRenderSpider()
    {
        super(new MyModelSpider(), 1.0F);
        this.setRenderPassModel(new MyModelSpider());
    }

    protected float setSpiderDeathMaxRotation(MyEntitySpider par1EntitySpider)
    {
        return 180.0F;
    }


    protected ResourceLocation getSpiderTextures(MyEntitySpider par1EntitySpider)
    {
        return spiderTextures;
    }

    protected float getDeathMaxRotation(EntityLivingBase par1EntityLivingBase)
    {
        return this.setSpiderDeathMaxRotation((MyEntitySpider)par1EntityLivingBase);
    }


    /**
     * Returns the location of an entity's texture. Doesn't seem to be called unless you call Render.bindEntityTexture.
     */
    protected ResourceLocation getEntityTexture(Entity par1Entity)
    {
        return this.getSpiderTextures((MyEntitySpider)par1Entity);
    }
}
