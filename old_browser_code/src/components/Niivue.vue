<script>
import { Niivue } from "@niivue/niivue";

// make an array of volumes to load
let volumeList = [
  { url: "https://niivue.github.io/niivue-demo-images/mni152.nii.gz" },
];
const nv = new Niivue();
nv.attachTo("gl"); // attach to canvas with id="gl"
nv.loadVolumes(volumeList);

</script>
