# practica-algoritmos
practica de algoritmos del libro (fundamentos de programacion)



(function () {

    document.addEventListener('DOMContentLoaded', function () {


        let horasTrabajadas = +prompt('Ingrese horas trabajadas');


        function pagoEmpleado(params) {

            const horasMinimas = 35;
            const tarifaHoraria = 15;
            let resultado = 0;
            let pagoTotal = 0;
            let menosImpuestos = 0;

            if (params <= horasMinimas) {
                resultado = tarifaHoraria * params;
                pagoTotal = resultado

            } else {
                resultado = tarifaHoraria * params; //resultado total 

                let horasExtras = params - horasMinimas; //cantidad de horas extras 

                let pagoExtras = (tarifaHoraria * 150) / 100; // exedente de la horas extras

                pagoTotal = resultado + (horasExtras * pagoExtras);

            }


            if (pagoTotal < 1000) {

                console.log(pagoTotal);

            } else if (pagoTotal > 1001 < 1400) {
                menosImpuestos = pagoTotal - (pagoTotal * 0.25);
                console.log(menosImpuestos.toFixed(2));
            }

            else {
                menosImpuestos = pagoTotal - (pagoTotal * 0.45);
                console.log(menosImpuestos.toFixed(2));
            }


        }

        pagoEmpleado(horasTrabajadas);



    });
})();
