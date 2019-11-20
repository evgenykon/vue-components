<template>
    <div class="language-selector">
        <a href="javascript:" @click="onClick" :class="current" :style="spriteBg"></a>
    </div>    
</template>
<script>
export default {
    props: {
        allowed: {
            type: Array,
            default: ['en', 'ru']
        },
        spriteUrl: {
            type: String,
            default: "data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8' standalone='no'%3F%3E%3C!-- --%3E%3Csvg xmlns:dc='http://purl.org/dc/elements/1.1/' xmlns:cc='http://creativecommons.org/ns%23' xmlns:rdf='http://www.w3.org/1999/02/22-rdf-syntax-ns%23' xmlns:svg='http://www.w3.org/2000/svg' xmlns='http://www.w3.org/2000/svg' xmlns:sodipodi='http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd' xmlns:inkscape='http://www.inkscape.org/namespaces/inkscape' width='24mm' height='32mm' viewBox='0 0 85.039373 113.38583' id='svg2' version='1.1' inkscape:version='0.91 r13725' sodipodi:docname='lang-flags.svg'%3E%3Cdefs id='defs4' /%3E%3Csodipodi:namedview id='base' pagecolor='%23ffffff' bordercolor='%23666666' borderopacity='1.0' inkscape:pageopacity='0.0' inkscape:pageshadow='2' inkscape:zoom='11.2' inkscape:cx='47.05178' inkscape:cy='86.47114' inkscape:document-units='px' inkscape:current-layer='layer1' showgrid='true' inkscape:window-width='1920' inkscape:window-height='1147' inkscape:window-x='-8' inkscape:window-y='-8' inkscape:window-maximized='1'%3E%3Cinkscape:grid type='xygrid' id='grid4138' /%3E%3C/sodipodi:namedview%3E%3Cmetadata id='metadata7'%3E%3Crdf:RDF%3E%3Ccc:Work rdf:about=''%3E%3Cdc:format%3Eimage/svg+xml%3C/dc:format%3E%3Cdc:type rdf:resource='http://purl.org/dc/dcmitype/StillImage' /%3E%3Cdc:title%3E%3C/dc:title%3E%3C/cc:Work%3E%3C/rdf:RDF%3E%3C/metadata%3E%3Cg inkscape:label='Layer 1' inkscape:groupmode='layer' id='layer1' transform='translate(0,-938.97638)'%3E%3Crect style='fill:%23ffffff;fill-opacity:1;stroke:%23009eb8;stroke-width:1.04913819;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' id='rect4136' width='83.95787' height='55.550869' x='0.52456909' y='996.28674' ry='9.2907391' /%3E%3Crect style='fill:%23ffffff;fill-opacity:1;stroke:%23009eb8;stroke-width:1.04975379;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' id='rect4136-8' width='84.057404' height='55.550255' x='0.52487689' y='939.68707' ry='9.2906361' /%3E%3Cpath style='fill:%2300355a;fill-opacity:1;stroke:%23009eb8;stroke-width:1;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' d='m 0.71428578,948.04075 c 1.04852542,-3.95562 3.01953402,-7.26007 8.08758142,-8.37838 l 36.9124178,0.0748 0,27.85714 -45.17857067,0 z' id='rect4155' inkscape:connector-curvature='0' sodipodi:nodetypes='cccccc' /%3E%3Ccircle style='fill:%23ffffff;fill-opacity:1;stroke:none;stroke-width:1;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' id='path5611' cx='10' cy='948.36218' r='2' /%3E%3Ccircle style='fill:%23ffffff;fill-opacity:1;stroke:none;stroke-width:1;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' id='path5611-8' cx='17.785715' cy='948.38007' r='2.0000002' /%3E%3Ccircle style='fill:%23ffffff;fill-opacity:1;stroke:none;stroke-width:1;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' id='path5611-0' cx='25.607145' cy='948.27289' r='2.0000002' /%3E%3Ccircle style='fill:%23ffffff;fill-opacity:1;stroke:none;stroke-width:1;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' id='path5611-6' cx='33.32143' cy='948.27289' r='2.0000002' /%3E%3Ccircle style='fill:%23ffffff;fill-opacity:1;stroke:none;stroke-width:1;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' id='path5611-2' cx='10.053573' cy='957.20148' r='2.0000002' /%3E%3Ccircle style='fill:%23ffffff;fill-opacity:1;stroke:none;stroke-width:1;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' id='path5611-5' cx='17.57143' cy='957.02289' r='2.0000002' /%3E%3Ccircle style='fill:%23ffffff;fill-opacity:1;stroke:none;stroke-width:1;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' id='path5611-64' cx='25.57143' cy='956.91577' r='2.0000002' /%3E%3Ccircle style='fill:%23ffffff;fill-opacity:1;stroke:none;stroke-width:1;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' id='path5611-59' cx='33.32143' cy='957.00507' r='2.0000002' /%3E%3Crect style='fill:%23ff1313;fill-opacity:1;stroke:none;stroke-width:1;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' id='rect5666' width='37.82143' height='5.6249995' x='46.17857' y='948.20148' /%3E%3Crect style='fill:%23ff1313;fill-opacity:1;stroke:none;stroke-width:1;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' id='rect5666-3' width='83.000008' height='6.2500005' x='0.98213863' y='968.09436' /%3E%3Crect style='fill:%23ff1313;fill-opacity:1;stroke:none;stroke-width:1;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' id='rect5666-9' width='83.089294' height='6.4285717' x='0.87499529' y='979.91577' /%3E%3Crect style='fill:%23ff1313;fill-opacity:1;stroke:none;stroke-width:1;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' id='rect5666-2' width='37.821434' height='5.6250005' x='46.160713' y='957.86218' /%3E%3Cpath style='fill:%23ff1313;fill-opacity:1;stroke:none;stroke-width:1;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' d='m 1,1034.3622 83,0 0,9.5893 c -1.999993,6.4107 -4.999993,7.4107 -8.285707,7.4107 l -66.5892922,0 C 3.0000003,1050.3622 1.42318,1046.5545 1,1043.7015 Z' id='rect5704' inkscape:connector-curvature='0' sodipodi:nodetypes='ccccccc' /%3E%3Crect style='fill:%2300355a;fill-opacity:1;stroke:none;stroke-width:1;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1' id='rect5707' width='83' height='19.25' x='1' y='1015.1122' /%3E%3C/g%3E%3C/svg%3E"
        }
    },
    data: () => {
        return {
            current: 'en'
        }        
    },
    computed: {
        spriteBg: function() {
            return 'background-image: url("' + this.spriteUrl + '")';
        }
    },
    methods: {
        onClick: function() {
            const pos = this.allowed.indexOf(this.current);
            if (pos + 1 >= this.allowed.length) {
                this.current = this.allowed[0];
            } else {
                this.current = this.allowed[pos + 1];
            }
            this.$emit('switch', this.current);
        }
    }
}
</script>
<style lang="scss" scoped>
.language-selector {
    margin-top: 2px;
    a {
        display: inline-block;
        width: 30px;
        height: 20px;
        background-size: 100% 200%;
        background-repeat: no-repeat;
        &.en {
            background-position: 0% 0%;
        }
        &.ru {
            background-position: 0% 100%;
        }
    }
}
</style>