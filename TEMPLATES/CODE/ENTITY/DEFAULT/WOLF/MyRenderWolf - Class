package mymod.entity.wolf;

import net.minecraft.client.model.ModelBase;
import net.minecraft.client.renderer.entity.RenderLiving;
import net.minecraft.entity.Entity;
import net.minecraft.util.ResourceLocation;
import cpw.mods.fml.relauncher.Side;
import cpw.mods.fml.relauncher.SideOnly;

@SideOnly(Side.CLIENT)
public class MyRenderWolf extends RenderLiving
{
    private static final ResourceLocation wolfTextures = new ResourceLocation("mymod:textures/entity/MyWolf.png");

    public MyRenderWolf(ModelBase par1ModelBase, float par3)
    {
        super(par1ModelBase, par3);
    }

    /**
     * Returns the location of an entity's texture. Doesn't seem to be called unless you call Render.bindEntityTexture.
     */
    protected ResourceLocation getEntityTexture(Entity par1Entity)
    {
        return wolfTextures;
    }
}
