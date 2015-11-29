package mymod.entity.enderman;

import java.util.Random;

import net.minecraft.block.Block;
import net.minecraft.client.model.ModelEnderman;
import net.minecraft.client.renderer.OpenGlHelper;
import net.minecraft.client.renderer.entity.RenderLiving;
import net.minecraft.client.renderer.texture.TextureMap;
import net.minecraft.entity.Entity;
import net.minecraft.entity.EntityLiving;
import net.minecraft.entity.EntityLivingBase;
import net.minecraft.util.ResourceLocation;

import org.lwjgl.opengl.GL11;
import org.lwjgl.opengl.GL12;

import cpw.mods.fml.relauncher.Side;
import cpw.mods.fml.relauncher.SideOnly;

@SideOnly(Side.CLIENT)
public class MyRenderEnderman extends RenderLiving
{
    private static final ResourceLocation endermanEyesTexture = new ResourceLocation("mymod:textures/entity/MyEndermanEyes.png");
    private static final ResourceLocation endermanTextures = new ResourceLocation("mymod:textures/entity/MyEnderman.png");

    /** The model of the enderman */
    private ModelEnderman endermanModel;
    private Random rnd = new Random();

    public MyRenderEnderman()
    {
        super(new ModelEnderman(), 0.5F);
        this.endermanModel = (ModelEnderman)super.mainModel;
        this.setRenderPassModel(this.endermanModel);
    }

    /**
     * Renders the enderman
     */
    public void renderEnderman(MyEntityEnderman par1MyEntityEnderman, double par2, double par4, double par6, float par8, float par9)
    {

            double d3 = 0.02D;
            par2 += this.rnd.nextGaussian() * d3;
            par6 += this.rnd.nextGaussian() * d3;

        super.doRenderLiving(par1MyEntityEnderman, par2, par4, par6, par8, par9);
    }

    protected ResourceLocation getEndermanTextures(MyEntityEnderman par1MyEntityEnderman)
    {
        return endermanTextures;
    }

    /**
     * Render the block an enderman is carrying
     
    protected void renderCarrying(MyEntityEnderman par1MyEntityEnderman, float par2)
    {
        super.renderEquippedItems(par1MyEntityEnderman, par2);


            GL11.glEnable(GL12.GL_RESCALE_NORMAL);
            GL11.glPushMatrix();
            float f1 = 0.5F;
            GL11.glTranslatef(0.0F, 0.6875F, -0.75F);
            f1 *= 1.0F;
            GL11.glRotatef(20.0F, 1.0F, 0.0F, 0.0F);
            GL11.glRotatef(45.0F, 0.0F, 1.0F, 0.0F);
            GL11.glScalef(-f1, -f1, f1);
            int i = par1MyEntityEnderman.getBrightnessForRender(par2);
            int j = i % 65536;
            int k = i / 65536;
            OpenGlHelper.setLightmapTextureCoords(OpenGlHelper.lightmapTexUnit, (float)j / 1.0F, (float)k / 1.0F);
            GL11.glColor4f(1.0F, 1.0F, 1.0F, 1.0F);
            GL11.glColor4f(1.0F, 1.0F, 1.0F, 1.0F);
            this.bindTexture(TextureMap.locationBlocksTexture);
      //    this.renderBlocks.renderBlockAsItem(Block.blocksList[par1MyEntityEnderman.getCarried()], par1MyEntityEnderman.getCarryingData(), 1.0F);
            GL11.glPopMatrix();
            GL11.glDisable(GL12.GL_RESCALE_NORMAL);
        
    }*/

    /**
     * Render the endermans eyes
     */
    protected int renderEyes(MyEntityEnderman par1MyEntityEnderman, int par2, float par3)
    {
        if (par2 != 0)
        {
            return -1;
        }
        else
        {
            this.bindTexture(endermanEyesTexture);
            float f1 = 1.0F;
            GL11.glEnable(GL11.GL_BLEND);
            GL11.glDisable(GL11.GL_ALPHA_TEST);
            GL11.glBlendFunc(GL11.GL_ONE, GL11.GL_ONE);
            GL11.glDisable(GL11.GL_LIGHTING);

            if (par1MyEntityEnderman.isInvisible())
            {
                GL11.glDepthMask(false);
            }
            else
            {
                GL11.glDepthMask(true);
            }

            char c0 = 61680;
            int j = c0 % 65536;
            int k = c0 / 65536;
            OpenGlHelper.setLightmapTextureCoords(OpenGlHelper.lightmapTexUnit, (float)j / 1.0F, (float)k / 1.0F);
            GL11.glColor4f(1.0F, 1.0F, 1.0F, 1.0F);
            GL11.glEnable(GL11.GL_LIGHTING);
            GL11.glColor4f(1.0F, 1.0F, 1.0F, f1);
            return 1;
        }
    }

    @Override
    protected ResourceLocation getEntityTexture(Entity entity) {
        return endermanTextures;

    }

 
}
