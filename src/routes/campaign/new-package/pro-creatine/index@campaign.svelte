<script lang="ts">
    import { SEO } from '$general/index';
    import { websiteSchema, organizationSchema } from '$utils/json-ld';
    // Section
    import { 
        SectionOne,
        SectionTwo,
        SectionThree,
        SectionFour,
        SectionFive,
        SectionSix,
        SectionCertified,
        SectionAllProducts
    } from '$components/layout-lp/v-six/index';
    // Content
	import { 
        cocokCardList
    } from '$contents/landing-page/v-one/creatine/index';
    // Content
    import { certifiedList } from '$contents/product-page/list-certified';
	import { productList } from '$contents/home-page/list-products';

    import BannerJumbotron from '$images/product/pro-creatine/pouch/banner-jumbotron.webp';
    import ProductOne from '$images/product/pro-creatine/pouch/produk-01-1.webp';
    import ProductTwoOne from '$images/product/pro-creatine/pouch/produk-02-1.webp';
    import ProductTwo from '$images/product/pro-creatine/pouch/produk-02-2.webp';
    import ProductThreeOne from '$images/product/pro-creatine/pouch/produk-03-1.webp';
    import ProductThree from '$images/product/pro-creatine/pouch/produk-03-2.webp';

    let productName: string = "Pro Creatine Pouch";
    let subTitlePin= false;
    let pinLogo = false;
    let beforePriceLabel = true;
</script>

<SEO 
    title={`Kemasan Terbaru - ${productName}`} 
    description={`Creatine terbaik untuk menambah massa otot yang mempunyai 6 varian rasa yang enak-enak. ${productName} aman dikonsumsi karna sudah bersertifikat halal dan BPOM.`}
    schemas={[
        websiteSchema, 
        organizationSchema
    ]}  
/>

<SectionOne
    banner={BannerJumbotron}
    txtPenawaran="Praktis Ekonomis Tingkatkan Massa Otot"
    txtSubPenawaran="Pro Creatine Pouch"
    classTxtPenawaran="text-white"
    classtxtSubPenawaran="text-white"
    orderBtnText="Cek Produknya Sekarang"
/>

<SectionSix 
    subtitle="{productName} "
    title='<span class="block uppercase">Tebalkan</span> 
    <span class="block uppercase">Massa Otot?</span> '
    descriptionOne='{productName} merupakan suplemen yang diformulasikan khusus untuk menambah dan menebalkan massa otot dalam tubuh, produk ini tidak menimbulkan efek samping berbahaya dan telah lulus uji Badan Pengawas Obat dan Makanan.'
    descriptionTwo='Selain diolah secara halal, produk ini juga mendapat sertifikasi <span class="font-bold uppercase"> GMP (Good Manufacturing product), Halal, BPOM, HACCP,  ISO 22000, & LABDOOR </span>'
    imgLink={ProductOne}
    altImg="AboutImage"
    
    bgColor="zinc-800"
    textHead="white"
    textSubHead="amber-500"
    txtDescColor="zinc-100"
/>

<SectionTwo 
    {subTitlePin}
    subtitle="{productName}"
    title="COCOK BUAT KAMU YANG"
    {cocokCardList}
    gridCount={cocokCardList.length}
/>

<SectionThree 
    id='musclefirst-education'
    {pinLogo}
    title="GOLD SERIES"
    subtitle="{productName}"
    titlePart=""
    image={ProductTwo}
    cocokCardOtherList={cocokCardList}
/>

<SectionCertified certifiedCardList={certifiedList} />
<SectionAllProducts products={productList} />

<SectionFive 
    bgColorSection="zinc-900"
    {beforePriceLabel}
    subtitle="Promo Khusus Pemesanan Pre Order"
    title='<span class="block">BERAPA HARGANYA?</span>'
    imgLink={ProductTwoOne}
    altImg="HargaImage"
    titlePrice='<span class="block text-white">Muscle First Pro Creatine Pouch 350g</span>'
    descriptionPrice='
    <h3 class="text-gray-100 font-base text-xl md:text-2xl"><b>Gratis Shaker</b> + <b>Gratis Scoop</b></h3>
    <span class="uppercase font-bold text-white">bisa didapatkan</span>
    <h3 class="text-gray-100 font-base text-xl md:text-2xl uppercase font-bold">Dengan harga</h3>'
    beforePrice="250.000"
    afterPrice="195.000"
    linkShopee="https://shopee.co.id/Muscle-First-Pro-Creatine-350g-Pouch-70-servings-Suplemen-Fitness-i.8802988.18570466009?sp_atk=9e836e8b-7078-4135-85f1-a605e177734b&xptdk=9e836e8b-7078-4135-85f1-a605e177734b"
    linkWhatsapp="https://wa.me/6285174226889/?text=Info%20Dari%20Website%20%3A%22Hallo%2C%20Saya%20tertarik%20dengan%promo%20khusus%20Muscle%20First%20pro%2Bcreatine%20pouch%22"
/>

<SectionFour 
    subtitle="Order Now"
    title='{productName}' 
/>