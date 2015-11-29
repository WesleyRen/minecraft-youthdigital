package mymod.entity.skeleton;

import cpw.mods.fml.relauncher.Side;
import cpw.mods.fml.relauncher.SideOnly;
import mymod.entity.skeleton.MyEntitySkeleton;
import net.minecraft.client.model.ModelSkeleton;
import net.minecraft.client.renderer.entity.RenderBiped;
import net.minecraft.entity.Entity;
import net.minecraft.entity.EntityLiving;
import net.minecraft.entity.EntityLivingBase;

import net.minecraft.util.ResourceLocation;

import org.lwjgl.opengl.GL11;

@SideOnly(Side.CLIENT)
public class MyRenderSkeleton extends RenderBiped
{
    private static final ResourceLocation skeletonTextures = new ResourceLocation("mymod:textures/entity/MySkeleton.png");

    public MyRenderSkeleton(MyModelSkeleton myModelSkeleton, float f)
    {
        super(myModelSkeleton, f);
    }

    protected void scaleSkeleton(MyEntitySkeleton par1MyEntitySkeleton, float par2)
    {
        GL11.glScalef(1.0F, 1.0F, 1.0F);
    }

    protected void func_82422_c()
    {
        GL11.glTranslatef(0.09375F, 0.1875F, 0.0F);
    }

    protected ResourceLocation func_110860_a(MyEntitySkeleton par1MyEntitySkeleton)
    {
        return skeletonTextures;
    }

    protected ResourceLocation func_110856_a(EntityLiving par1EntityLiving)
    {
        return this.func_110860_a((MyEntitySkeleton)par1EntityLiving);
    }

    /**
     * Allows the render to do any OpenGL state modifications necessary before the model is rendered. Args:
     * entityLiving, partialTickTime
     */
    protected void preRenderCallback(EntityLivingBase par1EntityLivingBase, float par2)
    {
        this.scaleSkeleton((MyEntitySkeleton)par1EntityLivingBase, par2);
    }

    /**
     * Returns the location of an entity's texture. Doesn't seem to be called unless you call Render.bindEntityTexture.
     */
    protected ResourceLocation getEntityTexture(Entity par1Entity)
    {
        return this.func_110860_a((MyEntitySkeleton)par1Entity);
    }
}
